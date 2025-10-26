# Cuestiones 1
## Cuestiones 1.1
- ¿Qué devuelve Clips al añadir un hecho a la Base de Hechos (BH)
Devuelve un identificador único del hecho, por ejemplo: `<Fact-1>`, `<Fact-2>`, etc.

- ¿Qué ocurre cuando se introduce un hecho “repetido” en la base de hechos (apellido-1 Perez)?
CLIPS no permite duplicados, por lo que no lo añade y devuelve el mismo identificador que tenía el primer hecho.

## Cuestiones 1.2
- ¿Se ha activado alguna regla? ¿Qué hechos activan cada regla?
Sí, si existen los hechos necesarios en la BH. Para que se active la regla-1 necesito `(nombre Adrian)`, para la regla-2 necesito estos 3 hechos `(nombre Adrian)`, `(apellido-1 Quiroga)` y `(apellido-2 Linares)`.

## Cuestiones 1.3
- ¿Qué regla se ejecuta en primer lugar? ¿Por qué?
Se ejecuta la segunda regla porque la estrategia por defecto de clips es ejecutar la regla más específica (con más condiciones)

- ¿Qué pasa si reiniciamos con (clear)?
Que se borra todo, los hechos y reglas han desaparecido y la BH queda vacía.

## Cuestiones 1.4
- Si se introducen los hechos con (deffacts), y se carga el fichero ¿qué ocurre en la BH y en la Agenda?
Las reglas se compilan y almacenan, los deffacts se registran pero no se añaden a la BH, y la agenda está vacía.

- ¿Qué ocurre en la BH y en la Agenda al ejecutar (reset)?
Se limpia la BH, se añade el hecho especial `(initial-fact) (f-0)` y se cargan todos los hechos definidos en deffacts, además se acutaliza la agenda con las reglas activadas

- ¿Cuál es el primer hecho que se ha almacenado en la BH?
`(initial-fact)` con identificador `f-0` que es un hecho especial que siempre existe tras `(reset)`.

## Cuestiones 1.5
![[Pasted image 20251025165800.png]]


# Cuestiones 2
## Cuestiones 2.3
-  ¿Quiénes son los hermanos, tíos, sobrinos, primos y abuelos de Archie?
Hermana de Archie: Ninguna, como no tienen la misma madre no identifica a Lilibet como hermana.
Tíos de Archie: Ninguno porque al no tener madre ni Guillermo ni enrique no los identifico como hermanos, así que no se identifica a Guillermo como tío de Archie.
Sobrinos de Archie: Ninguno .
Primos de Archie: Ninguno porque los primos los calculo en base al tío y al no detectar a Guillermo como tío no los identifica.
Abuelos de Archie: Carlos 

- ¿Quiénes son abuelos y de quién?
Isabel: Enrique y Guilllermo
Felipe: Enrique y Guillermo
Carlos: Jorge, Carlota, Luis, Archie, Lillibet

- ¿Quiénes son tíos y de quién?
Eduardo: Guillermo, Enrique
Andrés: Guillermo, Enrique
Ana: Guillermo, Enrique

## Cuestiones 2.4
- Incluir los hechos y, de ser necesario, las nuevas reglas que tengan en cuenta la nueva situación e indicar cuáles son ahora las respuestas a las cuestiones anteriores

-  ¿Quiénes son los hermanos, tíos, sobrinos, primos y abuelos de Archie?
Hermana de Archie: Ninguna, como no tienen la misma madre no identifica a Lilibet como hermana.
Tíos de Archie: Guillermo
Sobrinos de Archie: Ninguno 
Primos de Archie: Luis, Carlota y Jorge
Abuelos de Archie: Carlos y Diana.

- ¿Quiénes son abuelos y de quién?

Isabel: Enrique y Guilllermo.
Felipe: Enrique y Guillermo.
Carlos: Jorge, Carlota, Luis, Archie y Lillibet
Diana: Jorge, Carlota, Luis, Archie y Lillibet.

- ¿Quiénes son tíos y de quién?
Guillermo: Archie y Lillibet.
Enrique: Jorge, Carlota y Luis.
Eduardo: Guillermo, Enrique
Andrés: Guillermo, Enrique
Ana: Guillermo, Enrique

# Cuestiones 3
- Analiza el orden de ejecución de las reglas del bloque QUERY RULES y represéntalo gráficamente en forma de árbol, donde los nodos son las diferentes reglas (determine-engine-state, determine-runs-normally, …)

```txt
determine-engine-state (RAÍZ)
│
├─ RAMA 1: engine-starts = YES
│  │
│  └─ determine-runs-normally
│     │
│     ├─ runs-normally = YES
│     │  └─ → REPAIR: "No repair needed."
│     │
│     └─ runs-normally = NO
│        │
│        ├─ determine-sluggishness
│        │
│        ├─ determine-misfiring
│        │
│        ├─ determine-knocking
│        │
│        └─ determine-low-output
│
└─ RAMA 2: engine-starts = NO
   │
   └─ determine-rotation-state
      │
      ├─ engine-rotates = YES
      │  │
      │  ├─ determine-gas-level
      │  │
      │  └─ determine-point-surface-state
      │
      └─ engine-rotates = NO
         │
         └─ determine-battery-state
            │
            ├─ battery-has-charge = NO
            │  └─ → REPAIR: "Charge the battery."
            │
            ├─ battery-has-charge = YES
            │  └─ determine-conductivity-test
            │
            └─ determine-point-surface-state
```

- Justifique por qué todas las reglas del bloque QUERY RULES incluyen el antecedente (not (repair ?)) y si este es necesario o podría prescindirse de él.
Es necesario para el control de flujo de la ejecución, una vez que se ha determinado una reparación no tiene sentido seguir preguntando, esto también va a afectar al rendimiento general del sistema.

- Identifica qué reglas del sistema utilizan la variable saliencia. Revisando la documentación de CLIPS y otras fuentes investiga acerca del concepto de saliencia y justifica el papel que juega dicha variable y los valores elegidos en las reglas del sistema.
Saliencia es una propiedad de las reglas en CLIPS que determina su prioridad de ejecución cuando múltiples reglas están activadas simultáneamente.

El sistema utiliza tres niveles de prioridad para controlar el flujo de ejecución. System-banner tiene saliencia 10 para ejecutarse primero y mostrar el mensaje de bienvenida al iniciar el sistema. Print-repair también usa saliencia 10 para presentar inmediatamente el diagnóstico cuando se encuentra una reparación, interrumpiendo cualquier pregunta pendiente. Las reglas de consulta y diagnóstico mantienen la prioridad por defecto (0), ejecutándose en orden natural según el motor de inferencia.

No-repairs utiliza saliencia -10 para asegurar que solo se ejecute al final, después de que todas las demás reglas hayan terminado. Esto garantiza que el mensaje "no se necesita reparación" aparezca únicamente cuando se hayan agotado todas las comprobaciones posibles sin encontrar problemas. Esta prioridad negativa la convierte en la última regla en ejecutarse si ninguna otra ha determinado una reparación.

