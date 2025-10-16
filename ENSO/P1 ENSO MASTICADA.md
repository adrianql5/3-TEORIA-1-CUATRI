# Planning Detallado - Práctica 1: Planificación y Ciclos de Vida

## FASE 0: PREPARACIÓN INICIAL (Antes de empezar)

### Paso 0.1: Instalación de software

- [ ]  Descargar e instalar ProjectLibre (software gratuito)
- [ ]  Familiarizarte con la interfaz básica del programa
- [ ]  Descargar la plantilla de memoria del Campus Virtual

### Paso 0.2: Recuperar información del proyecto de BD II

- [ ]  Localizar documentación de tu proyecto de Bases de Datos II
- [ ]  Revisar requisitos funcionales (transacciones y consultas)
- [ ]  Identificar restricciones del proyecto
- [ ]  Si no cursaste BD II: hablar con el profesor para definir alternativa

---

## FASE 1: ESPECIFICACIÓN (Documentación previa)

### Paso 1.1: Documentar el alcance

- [ ]  Escribir descripción breve del ámbito de la aplicación
- [ ]  Definir el propósito principal de la aplicación
- [ ]  Identificar los usuarios objetivo

### Paso 1.2: Listar requisitos

- [ ]  Crear lista de requisitos funcionales:
    - Transacciones necesarias
    - Consultas a implementar
- [ ]  Documentar restricciones técnicas y de negocio
- [ ]  Organizar por prioridad (te servirá para ejercicio C)

### Paso 1.3: Crear EDT (Estructura de Desglose del Trabajo)

- [ ]  Identificar componentes principales de la aplicación
- [ ]  Crear diagrama de bloques con estos componentes
- [ ]  Vincular cada componente con funcionalidades específicas
- [ ]  **Guardar este diagrama para incluir en la memoria**

---

## FASE 2: EJERCICIO A - Cascada

### Paso 2.1: Crear nuevo proyecto en ProjectLibre

- [ ]  Abrir ProjectLibre
- [ ]  Crear nuevo proyecto
- [ ]  Configurar fecha inicio: 1 de enero del próximo año
- [ ]  Guardar como "A_Cascada_[TuApellido].pod"

### Paso 2.2: Definir estructura de procesos en Cascada

Crear los siguientes paquetes de trabajo (tareas resumen):

- [ ]  1. Análisis
- [ ]  2. Diseño
- [ ]  3. Implementación/Codificación
- [ ]  4. Pruebas
- [ ]  5. Implantación

### Paso 2.3: Descomponer cada proceso en tarefas

Para **Análisis**:

- [ ]  Análisis de requisitos
- [ ]  Especificación funcional
- [ ]  Análisis de viabilidad
- [ ]  Documentación de análisis

Para **Diseño**:

- [ ]  Diseño de arquitectura
- [ ]  Diseño de base de datos
- [ ]  Diseño de interfaces
- [ ]  Documentación de diseño

Para **Implementación**:

- [ ]  Configuración del entorno
- [ ]  Desarrollo de [Funcionalidad 1]
- [ ]  Desarrollo de [Funcionalidad 2]
- [ ]  ... (según tu EDT)
- [ ]  Documentación de código

Para **Pruebas**:

- [ ]  Diseño de casos de prueba
- [ ]  Pruebas unitarias
- [ ]  Pruebas de integración
- [ ]  Corrección de errores
- [ ]  Documentación de pruebas

Para **Implantación**:

- [ ]  Preparación del entorno de producción
- [ ]  Instalación y configuración
- [ ]  Formación de usuarios
- [ ]  Documentación de usuario

### Paso 2.4: Estimar esfuerzos

- [ ]  Para cada tarea, estimar horas de trabajo realistas
- [ ]  Introducir la duración en días (ProjectLibre convierte automáticamente)
- [ ]  **Objetivo: que el proyecto dure aproximadamente 3 meses**

### Paso 2.5: Crear vinculaciones

- [ ]  Establecer dependencias entre tareas (Fin-Inicio principalmente)
- [ ]  Asegurarte de que sigue el modelo cascada (secuencial)
- [ ]  Si supera 3 meses, identificar tareas que pueden ir en paralelo

### Paso 2.6: Crear hitos

- [ ]  Crear hito al final de Análisis: "Análisis completado"
- [ ]  Crear hito al final de Diseño: "Diseño completado"
- [ ]  Crear hito al final de Implementación: "Código completado"
- [ ]  Crear hito al final de Pruebas: "Pruebas superadas"
- [ ]  Crear hito final: "Proyecto entregado"

### Paso 2.7: Verificación y guardado

- [ ]  Revisar que el diagrama de Gantt es coherente
- [ ]  Verificar que la duración total es ~3 meses
- [ ]  Guardar el proyecto

---

## FASE 3: EJERCICIO B - Recursos y Costos

### Paso 3.1: Abrir copia del ejercicio A

- [ ]  Guardar como "B_Cascada_Recursos_[TuApellido].pod"

### Paso 3.2: Calcular tasas de coste

**Fórmula: Coste empresa = Salario bruto × 1.30**

Para cada rol:

- [ ]  **Programador**: 1000€ × 1.30 = 1300€/mes
    - Convertir a €/hora: 1300€ / 160 horas ≈ **8.13 €/hora**
- [ ]  **Diseñador/Analista**: 2000€ × 1.30 = 2600€/mes
    - Convertir a €/hora: 2600€ / 160 horas ≈ **16.25 €/hora**
- [ ]  **Director de proyecto**: 3000€ × 1.30 = 3900€/mes
    - Convertir a €/hora: 3900€ / 160 horas ≈ **24.38 €/hora**

_(Asumiendo mes laboral de 160 horas)_

### Paso 3.3: Crear recursos en ProjectLibre

- [ ]  Ir a Vista de Recursos
- [ ]  Crear recurso "Programador" con tasa estándar 8.13 €/h
- [ ]  Crear recurso "Diseñador/Analista" con tasa 16.25 €/h
- [ ]  Crear recurso "Director Proyecto" con tasa 24.38 €/h

### Paso 3.4: Asignar recursos a tareas

Volver a vista de Gantt y asignar:

- [ ]  Tareas de análisis → Diseñador/Analista
- [ ]  Tareas de diseño → Diseñador/Analista
- [ ]  Tareas de implementación → Programador
- [ ]  Tareas de pruebas → Programador
- [ ]  Gestión y coordinación → Director Proyecto
- [ ]  Documentación → según corresponda

### Paso 3.5: Generar informe de costos

- [ ]  Ir a Informes → Coste del proyecto
- [ ]  Capturar informe que muestre:
    - Coste por paquete de trabajo
    - Coste total del proyecto
- [ ]  Guardar captura para incluir en la memoria

### Paso 3.6: Guardado

- [ ]  Guardar el proyecto

---

## FASE 4: EJERCICIO C - Incrementos

### Paso 4.1: Crear copia del ejercicio B

- [ ]  Guardar como "C_Incrementos_[TuApellido].pod"

### Paso 4.2: Dividir alcance en 3 incrementos

Planificar en papel primero:

- [ ]  **Incremento 1**: Funcionalidad mínima viable (MVP)
    - ¿Qué funcionalidad básica permite usar la app?
    - Ejemplo: módulo de login + una transacción básica
- [ ]  **Incremento 2**: Siguientes funcionalidades por prioridad
- [ ]  **Incremento 3**: Resto de funcionalidades (completar alcance original)

### Paso 4.3: Reorganizar estructura del proyecto

Crear nueva estructura:

- [ ]  **Procesos comunes iniciales**:
    - Análisis inicial
    - Diseño arquitectónico general
    - Configuración entorno
- [ ]  **Incremento 1**:
    - Análisis detallado Inc1
    - Diseño Inc1
    - Implementación Inc1
    - Pruebas Inc1
    - Hito: "Incremento 1 completado"
- [ ]  **Incremento 2**:
    - Análisis detallado Inc2
    - Diseño Inc2
    - Implementación Inc2
    - Pruebas Inc2
    - Hito: "Incremento 2 completado"
- [ ]  **Incremento 3**:
    - Análisis detallado Inc3
    - Diseño Inc3
    - Implementación Inc3
    - Pruebas Inc3
    - Hito: "Incremento 3 completado"
- [ ]  **Implantación final**

### Paso 4.4: Ajustar tareas y esfuerzos

- [ ]  Redistribuir tareas del ejercicio B entre los incrementos
- [ ]  Ajustar duraciones si es necesario
- [ ]  Mantener recursos asignados

### Paso 4.5: Calcular costos por incremento

- [ ]  Anotar coste de Incremento 1
- [ ]  Anotar coste de Incremento 2
- [ ]  Anotar coste de Incremento 3
- [ ]  Verificar coste total del proyecto

### Paso 4.6: Guardado

- [ ]  Guardar proyecto

---

## FASE 5: EJERCICIO D - Espiral

### Paso 5.1: Crear copia del ejercicio B

- [ ]  Guardar como "D_Espiral_[TuApellido].pod"

### Paso 5.2: Identificar funcionalidades por riesgo

- [ ]  Listar todas las funcionalidades
- [ ]  Clasificar por nivel de riesgo (técnico, complejidad, etc.)
- [ ]  **Iteración 1**: Funcionalidades de BAJO riesgo
- [ ]  **Iteración 2**: Funcionalidades de riesgo MEDIO/ALTO

### Paso 5.3: Estructurar Iteración 1

Crear procesos según modelo espiral:

- [ ]  **Planificación Iteración 1**
    - Definición de objetivos
    - Identificación de restricciones
- [ ]  **Análisis de riesgos Iteración 1**
    - Identificación de riesgos
    - Evaluación de riesgos
    - Estrategias de mitigación
- [ ]  **Ingeniería Iteración 1**
    - Análisis detallado
    - Diseño
    - Implementación
    - Pruebas
- [ ]  **Evaluación del cliente Iteración 1**
    - Revisión con cliente
    - Recopilación feedback
- [ ]  Hito: "Iteración 1 completada"

### Paso 5.4: Estructurar Iteración 2

- [ ]  Repetir estructura de la Iteración 1 para Iteración 2
- [ ]  Incluir tareas adicionales de gestión de riesgos más complejos
- [ ]  Hito: "Iteración 2 completada"

### Paso 5.5: Asignar recursos y ajustar

- [ ]  Mantener recursos del ejercicio B
- [ ]  Asignar especialmente al Diseñador/Analista en análisis de riesgos
- [ ]  Verificar coherencia temporal

### Paso 5.6: Guardado

- [ ]  Guardar proyecto

---

## FASE 6: EJERCICIO E - Ampliación Cascada

### Paso 6.1: Definir requisitos adicionales

En la memoria, documentar:

- [ ]  2 transacciones adicionales (escoge al azar funcionalidades nuevas)
- [ ]  Interfaz gráfica de usuario (GUI)
- [ ]  Sistema de backup de base de datos

### Paso 6.2: Abrir ejercicio B y crear línea base

- [ ]  Abrir "B_Cascada_Recursos_[TuApellido].pod"
- [ ]  Guardar como "E_Ampliacion_Cascada_[TuApellido].pod"
- [ ]  Crear línea base: Proyecto → Establecer línea base → Línea base 1

### Paso 6.3: Añadir tareas para nueva funcionalidad

En cada proceso del ciclo cascada:

- [ ]  **En Análisis**: añadir análisis de las 2 transacciones, GUI y backup
- [ ]  **En Diseño**: añadir diseño de las 2 transacciones, GUI y backup
- [ ]  **En Implementación**: añadir desarrollo de todo lo nuevo
- [ ]  **En Pruebas**: añadir pruebas de las nuevas funcionalidades
- [ ]  Incrementar esfuerzo en tareas existentes si procede

### Paso 6.4: Crear recursos de personas concretas

Crear 4 nuevos recursos (personas):

- [ ]  **Bea** - Tabla de costos: Director/a Proyecto (24.38 €/h)
- [ ]  **Xulia** - Tablas de costos:
    - Analista (16.25 €/h)
    - Diseñador/a (16.25 €/h)
- [ ]  **Xosé** - Tablas de costos:
    - Diseñador/a (16.25 €/h)
    - Programador/a Desarrollo (8.13 €/h)
- [ ]  **Ana** - Tablas de costos:
    - Programador/a Desarrollo (8.13 €/h)
    - Programador/a Pruebas (8.13 €/h)
    - SQA (16.25 €/h)

### Paso 6.5: Configurar tablas de costos múltiples

Para cada persona:

- [ ]  Ir a Vista de Recursos → Doble clic en recurso
- [ ]  Pestaña "Tasas de coste"
- [ ]  Tabla A: tasa del primer rol
- [ ]  Tabla B: tasa del segundo rol (si aplica)
- [ ]  Tabla C: tasa del tercer rol (si aplica)

### Paso 6.6: Reasignar recursos genéricos por personas

- [ ]  Eliminar asignaciones de recursos genéricos
- [ ]  Asignar personas concretas según sus roles:
    - Tareas de dirección → Bea (Tabla A)
    - Tareas de análisis → Xulia (Tabla A)
    - Tareas de diseño → Xulia o Xosé (Tabla B o A respectivamente)
    - Tareas de desarrollo → Xosé o Ana (Tabla B o A)
    - Tareas de pruebas → Ana (Tabla B)

### Paso 6.7: Añadir tareas de SQA (Aseguramiento de Calidad)

Para cada tarea de documentación existente:

- [ ]  Crear tarea adicional: "[Nombre doc] - Revisión SQA"
- [ ]  Establecer dependencia: revisión empieza cuando termina documentación
- [ ]  Asignar Ana como SQA al 100% (Tabla C: 16.25 €/h)
- [ ]  Asignar autor original de la doc al 10% como soporte

Ejemplo:

- Tarea original: "Documentación de análisis" → Xulia 100%
- Nueva tarea: "Documentación de análisis - Revisión SQA"
    - Ana (SQA) al 100%
    - Xulia (soporte) al 10%

### Paso 6.8: Verificar duración y sobreasignaciones

- [ ]  Comprobar que el proyecto no supere 4 meses
- [ ]  Ver Vista → Gráfico de recursos
- [ ]  Verificar que ningún recurso esté sobreasignado (en rojo)
- [ ]  Si hay sobreasignaciones, ajustar manualmente:
    - Paralelizar tareas
    - Redistribuir trabajo
    - Ajustar porcentajes de asignación

### Paso 6.9: Comparar con línea base

- [ ]  Ir a Vista de Gantt
- [ ]  Mostrar línea base: Ver → Mostrar línea base
- [ ]  Anotar diferencias:
    - Duración original vs nueva
    - Trabajo (horas) original vs nuevo
    - Coste original vs nuevo

### Paso 6.10: Guardado

- [ ]  Guardar proyecto

---

## FASE 7: EJERCICIO F - Sobreasignaciones y Nivelación

### Paso 7.1: Abrir ejercicio E y crear segunda línea base

- [ ]  Abrir "E_Ampliacion_Cascada_[TuApellido].pod"
- [ ]  Guardar como "F_Nivelacion_[TuApellido].pod"
- [ ]  Crear línea base 2: Proyecto → Establecer línea base → Línea base 2

### Paso 7.2: Cambiar disponibilidad de Bea

- [ ]  Ir a Vista de Recursos
- [ ]  Doble clic en recurso "Bea"
- [ ]  Cambiar disponibilidad de 100% a 50%
- [ ]  Aceptar

### Paso 7.3: Identificar sobreasignaciones

- [ ]  Volver a vista de Gantt
- [ ]  Vista → Gráfico de recursos
- [ ]  Identificar tareas donde Bea aparece en rojo (sobreasignada)
- [ ]  Listar estas tareas

### Paso 7.4: Resolver sobreasignaciones

**RESTRICCIONES**:

- NO reducir horas de trabajo de las tareas
- Minimizar retraso en fecha fin del proyecto

**3 Estrategias a aplicar** (debes explicarlas en la memoria):

**Estrategia 1: Redistribución de trabajo**

- [ ]  Tarea sobreasignada: [nombre tarea X]
- [ ]  Solución: Reducir asignación de Bea de 100% a 50% y aumentar otra persona
- [ ]  Documentar esta decisión

**Estrategia 2: Paralelización de tareas**

- [ ]  Tarea sobreasignada: [nombre tarea Y]
- [ ]  Solución: Identificar dependencias que no son estrictamente necesarias
- [ ]  Convertir dependencia Fin-Inicio en paralelas
- [ ]  Documentar esta decisión

**Estrategia 3: Reasignación a otro recurso**

- [ ]  Tarea sobreasignada: [nombre tarea Z]
- [ ]  Solución: Sustituir a Bea por otro recurso disponible con capacidad
- [ ]  Verificar que el recurso sustituto tiene tabla de costos apropiada
- [ ]  Documentar esta decisión

### Paso 7.5: Verificar resolución

- [ ]  Comprobar que no quedan recursos en rojo
- [ ]  Ver fecha de fin del proyecto
- [ ]  Comparar con línea base 2

### Paso 7.6: Documentar estrategias

En la memoria, para cada estrategia:

- [ ]  Indicar tarea concreta afectada
- [ ]  Explicar qué estrategia usaste
- [ ]  Justificar por qué fue la mejor opción
- [ ]  Mostrar resultado (captura antes/después si es posible)

### Paso 7.7: Guardado final

- [ ]  Guardar proyecto

---

## FASE 8: ELABORACIÓN DE LA MEMORIA

### Paso 8.1: Descargar y preparar plantilla

- [ ]  Descargar plantilla de memoria del Campus Virtual
- [ ]  Crear portada con tus datos

### Paso 8.2: Incluir especificación inicial

- [ ]  Descripción del alcance (Fase 1.1)
- [ ]  Listado de requisitos y restricciones (Fase 1.2)
- [ ]  Diagrama EDT (Fase 1.3)

### Paso 8.3: Documentar Ejercicio A

- [ ]  Breve explicación del modelo en cascada aplicado
- [ ]  Captura del diagrama de Gantt completo
- [ ]  Tabla con fitos y fechas

### Paso 8.4: Documentar Ejercicio B

- [ ]  Tabla con cálculo de tasas de coste (Fase 3.2)
- [ ]  Captura del informe de costos (Fase 3.5)
- [ ]  Explicar criterios de asignación de recursos

### Paso 8.5: Documentar Ejercicio C

- [ ]  Explicar división en incrementos y criterio usado
- [ ]  Descripción de alcance de cada incremento
- [ ]  Captura de diagrama de Gantt del modelo incremental
- [ ]  Tabla con costes por incremento y total

### Paso 8.6: Documentar Ejercicio D

- [ ]  Explicar criterios de clasificación por riesgo
- [ ]  Tabla de funcionalidades por riesgo
- [ ]  Captura del diagrama de Gantt del modelo espiral
- [ ]  Describir tareas específicas de gestión de riesgos

### Paso 8.7: Documentar Ejercicio E

- [ ]  Listar requisitos adicionales definidos
- [ ]  Tabla de recursos (personas) con sus roles y tasas
- [ ]  Captura de comparativa con línea base 1:
    - Duración
    - Trabajo total
    - Costes
- [ ]  Explicar configuración de tablas de costos
- [ ]  Describir estrategia de asignación de tareas SQA

### Paso 8.8: Documentar Ejercicio F

- [ ]  Explicar impacto del cambio de Bea a 50%
- [ ]  Captura mostrando sobreasignaciones detectadas
- [ ]  Documentar las 3 estrategias aplicadas:
    - Tarea afectada
    - Estrategia usada
    - Justificación
    - Resultado
- [ ]  Tabla comparativa con línea base 2
- [ ]  Captura final sin sobreasignaciones

### Paso 8.9: Conclusiones

- [ ]  Reflexión sobre aprendizajes
- [ ]  Comparativa entre ciclos de vida
- [ ]  Dificultades encontradas

### Paso 8.10: Revisión final

- [ ]  Revisar ortografía y redacción
- [ ]  Verificar que todas las capturas sean legibles
- [ ]  Comprobar numeración de figuras y tablas
- [ ]  Generar PDF

---

## FASE 9: ENTREGA

### Paso 9.1: Preparar archivos

Debes tener 7 archivos:

- [ ]  A_Cascada_[TuApellido].pod
- [ ]  B_Cascada_Recursos_[TuApellido].pod
- [ ]  C_Incrementos_[TuApellido].pod
- [ ]  D_Espiral_[TuApellido].pod
- [ ]  E_Ampliacion_Cascada_[TuApellido].pod
- [ ]  F_Nivelacion_[TuApellido].pod
- [ ]  Memoria_P1_[TuApellido].pdf

### Paso 9.2: Verificación pre-entrega

- [ ]  Abrir cada archivo .pod y verificar que se carga correctamente
- [ ]  Verificar que el PDF incluye todas las secciones
- [ ]  Comprobar que las capturas son claras y legibles

### Paso 9.3: Subir al Campus Virtual

- [ ]  Acceder a la tarea en el Campus Virtual
- [ ]  Subir los 7 archivos
- [ ]  Verificar que la subida fue correcta
- [ ]  Confirmar entrega

---

## CONSEJOS FINALES

### Gestión del tiempo

- **Especificación**: 2-3 horas
- **Ejercicio A**: 3-4 horas
- **Ejercicio B**: 2-3 horas
- **Ejercicio C**: 3-4 horas
- **Ejercicio D**: 3-4 horas
- **Ejercicio E**: 4-5 horas (el más complejo)
- **Ejercicio F**: 2-3 horas
- **Memoria**: 4-5 horas

**Total estimado: 23-31 horas**

### Recomendaciones

- Guarda versiones frecuentemente
- Haz copias de seguridad de los archivos .pod
- No dejes todo para el final
- Consulta tutorías si tienes dudas
- Revisa los apuntes de teoría sobre cada ciclo de vida
- Sé realista con las estimaciones de esfuerzo

### Errores comunes a evitar

- Olvidar crear líneas base antes de modificar
- No verificar sobreasignaciones
- Asignar recursos inadecuados a tareas
- Hacer EDT demasiado genérico o demasiado detallado
- No documentar decisiones importantes en la memoria
- Capturas ilegibles o incompletas