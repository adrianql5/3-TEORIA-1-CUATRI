<!-- Copyright (c) 2025 Adrián Quiroga Linares Lectura y referencia permitidas; reutilización y plagio prohibidos -->

# GUÍA DE ESTIMACIÓN DE ESFUERZOS

## Sistema de Gestión de Cine (3 meses / 12 semanas)

---

## TABLA RESUMEN DE ESFUERZOS ESTIMADOS

|Fase del Ciclo en Cascada|Duración|Esfuerzo (horas)|
|---|---|---|
|**1. ANÁLISIS**|2 semanas|160h|
|**2. DISEÑO**|3 semanas|240h|
|**3. IMPLEMENTACIÓN**|5 semanas|400h|
|**4. PRUEBAS**|1.5 semanas|120h|
|**5. IMPLANTACIÓN**|0.5 semanas|40h|
|**TOTAL**|**12 semanas**|**960h**|

---

## FASE 1: ANÁLISIS (2 semanas - 160 horas)

### 1.1 Análisis de Requisitos (40h)

- Recopilación de requisitos funcionales: **16h**
- Recopilación de requisitos no funcionales: **8h**
- Análisis de restricciones técnicas: **8h**
- Priorización de funcionalidades: **8h**

### 1.2 Análisis del Dominio (30h)

- Estudio del negocio del cine: **12h**
- Identificación de actores del sistema: **6h**
- Definición de casos de uso principales: **12h**

### 1.3 Análisis de Viabilidad (25h)

- Estudio técnico: **10h**
- Estudio económico: **8h**
- Análisis de riesgos inicial: **7h**

### 1.4 Especificación Funcional (40h)

- Documentación de 40 transacciones: **24h** (0.6h x 40)
- Diagramas de flujo de transacciones críticas: **10h**
- Validación con stakeholders: **6h**

### 1.5 Documentación de Análisis (25h)

- Redacción documento de análisis: **16h**
- Revisión y correcciones: **6h**
- Aprobación final: **3h**

---

## FASE 2: DISEÑO (3 semanas - 240 horas)

### 2.1 Diseño de Arquitectura (35h)

- Definición de arquitectura general: **12h**
- Diseño de capas (presentación, negocio, datos): **15h**
- Documentación de arquitectura: **8h**

### 2.2 Diseño de Base de Datos (60h)

- **Modelo Entidad-Relación**: **20h**
    - Identificación de entidades (17): **6h**
    - Definición de relaciones: **8h**
    - Atributos y restricciones: **6h**
- **Modelo Relacional**: **25h**
    - Transformación ER → Relacional: **10h**
    - Normalización: **8h**
    - Definición de claves e índices: **7h**
- **Diccionario de Datos**: **15h**
    - Documentación de 17 tablas: **12h**
    - Validaciones y restricciones: **3h**

### 2.3 Diseño de Interfaces (65h)

- **Wireframes y mockups**: **25h**
    - Interfaz de administrador (10 pantallas): **15h**
    - Interfaz de cliente (8 pantallas): **10h**
- **Diseño visual**: **20h**
    - Paleta de colores y estilos: **8h**
    - Diseño de componentes: **12h**
- **Flujos de navegación**: **12h**
- **Documentación de UI/UX**: **8h**

### 2.4 Diseño Detallado de Componentes (50h)

- **Módulo Autenticación**: **5h**
- **Módulo Cartelera**: **8h**
- **Módulo Reservas** (con concurrencia): **10h**
- **Módulo Restauración** (con stock): **8h**
- **Módulo Valoraciones**: **6h**
- **Módulo RR.HH**: **6h**
- **Módulo Instalaciones**: **7h**

### 2.5 Diseño de Seguridad (15h)

- Sistema de encriptación: **6h**
- Control de accesos: **5h**
- Gestión de sesiones: **4h**

### 2.6 Documentación de Diseño (15h)

- Redacción documento de diseño: **10h**
- Diagramas técnicos: **3h**
- Revisión: **2h**

---

## FASE 3: IMPLEMENTACIÓN (5 semanas - 400 horas)

### 3.1 Configuración del Entorno (15h)

- Instalación y configuración BD: **5h**
- Configuración IDE Java: **3h**
- Configuración repositorio: **2h**
- Setup de librerías: **5h**

### 3.2 Implementación de Base de Datos (40h)

- Creación de tablas (17): **15h**
- Creación de índices y restricciones: **10h**
- Triggers y procedimientos almacenados: **10h**
- Scripts de prueba y datos iniciales: **5h**

### 3.3 Capa de Acceso a Datos (DAO) (45h)

- DAOs genéricos: **8h**
- DAOs específicos por entidad (17): **25h** (1.5h x 17)
- Gestión de transacciones: **8h**
- Manejo de excepciones: **4h**

### 3.4 Lógica de Negocio (120h)

#### 3.4.1 Módulo Autenticación (15h)

- Login y validación: **6h**
- Encriptación de contraseñas: **5h**
- Gestión de sesiones: **4h**

#### 3.4.2 Módulo Usuarios (12h)

- Registro de clientes: **4h**
- Actualización de datos: **4h**
- Eliminación con validaciones: **4h**

#### 3.4.3 Módulo Cartelera (25h)

- CRUD películas: **10h**
- CRUD sesiones: **10h**
- Gestión de anuncios: **5h**

#### 3.4.4 Módulo Reservas (30h)

- Consulta de disponibilidad: **6h**
- Sistema de reservas con bloqueos: **15h** (crítico)
- Cancelación de reservas: **5h**
- Consultas de reservas: **4h**

#### 3.4.5 Módulo Restauración (18h)

- Gestión de catálogo: **5h**
- Pedidos con control de stock: **10h** (crítico)
- Consultas y cancelaciones: **3h**

#### 3.4.6 Módulo Valoraciones (12h)

- CRUD valoraciones: **8h**
- Cálculo de medias: **4h**

#### 3.4.7 Módulo RR.HH (10h)

- CRUD trabajadores: **6h**
- Asignaciones sala-trabajador: **4h**

#### 3.4.8 Módulo Instalaciones (8h)

- Gestión de equipamiento: **5h**
- Consultas de infraestructura: **3h**

### 3.5 Capa de Presentación (140h)

#### 3.5.1 Componentes Comunes (20h)

- Sistema de ventanas base: **8h**
- Componentes reutilizables: **8h**
- Gestión de eventos: **4h**

#### 3.5.2 Interfaz de Administrador (70h)

- Ventana principal con menú: **10h**
- Gestión de películas: **12h**
- Gestión de cartelera: **12h**
- Gestión de restauración: **8h**
- Gestión de RR.HH: **12h**
- Gestión de instalaciones: **10h**
- Diálogos y ventanas auxiliares: **6h**

#### 3.5.3 Interfaz de Cliente (50h)

- Login y registro: **8h**
- Ventana principal: **10h**
- Módulo de reservas (con plano butacas): **15h**
- Módulo de pedidos: **8h**
- Módulo de valoraciones: **6h**
- Configuración de cuenta: **3h**

### 3.6 Integración (25h)

- Integración de capas: **12h**
- Resolución de dependencias: **8h**
- Ajustes de comunicación: **5h**

### 3.7 Documentación de Código (15h)

- Comentarios y JavaDoc: **10h**
- README y guías: **5h**

---

## FASE 4: PRUEBAS (1.5 semanas - 120 horas)

### 4.1 Diseño de Casos de Prueba (20h)

- Casos de prueba unitarios: **8h**
- Casos de prueba de integración: **8h**
- Casos de prueba de sistema: **4h**

### 4.2 Pruebas Unitarias (35h)

- Pruebas de DAOs: **10h**
- Pruebas de lógica de negocio: **20h**
- Corrección de errores: **5h**

### 4.3 Pruebas de Integración (30h)

- Integración capa datos-negocio: **10h**
- Integración negocio-presentación: **10h**
- Pruebas de transacciones complejas: **10h**

### 4.4 Pruebas de Sistema (25h)

- Pruebas funcionales (40 transacciones): **15h**
- Pruebas de concurrencia: **6h**
- Pruebas de rendimiento: **4h**

### 4.5 Corrección de Errores (8h)

- Resolución de bugs críticos: **5h**
- Ajustes menores: **3h**

### 4.6 Documentación de Pruebas (2h)

- Informe de resultados: **2h**

---

## FASE 5: IMPLANTACIÓN (0.5 semanas - 40 horas)

### 5.1 Preparación del Entorno (10h)

- Configuración servidor de producción: **5h**
- Instalación de BD en producción: **3h**
- Configuración de seguridad: **2h**

### 5.2 Instalación y Configuración (8h)

- Despliegue de aplicación: **4h**
- Migración de datos: **3h**
- Verificación de instalación: **1h**

### 5.3 Formación de Usuarios (15h)

- Manual de administrador: **6h**
- Manual de usuario cliente: **4h**
- Sesiones de formación: **5h**

### 5.4 Documentación Final (5h)

- Manual de instalación: **2h**
- Documentación técnica final: **2h**
- Guía de mantenimiento: **1h**

### 5.5 Cierre del Proyecto (2h)

- Reunión de cierre: **1h**
- Entrega formal: **1h**

---

## DISTRIBUCIÓN DE RECURSOS RECOMENDADA

### Fase de Análisis

- **Analista**: 80% del tiempo
- **Director de Proyecto**: 20% del tiempo

### Fase de Diseño

- **Diseñador/Analista**: 90% del tiempo
- **Director de Proyecto**: 10% del tiempo

### Fase de Implementación

- **Programador**: 85% del tiempo
- **Diseñador** (para consultas): 10% del tiempo
- **Director de Proyecto**: 5% del tiempo

### Fase de Pruebas

- **Programador**: 70% del tiempo
- **Analista** (validación): 20% del tiempo
- **Director de Proyecto**: 10% del tiempo

### Fase de Implantación

- **Programador**: 40% del tiempo
- **Analista**: 30% del tiempo
- **Director de Proyecto**: 30% del tiempo

---

## TAREAS CRÍTICAS A INCLUIR

### ⚠️ Tareas con dependencias fuertes

1. Diseño de BD → debe terminar antes de implementación
2. Diseño de interfaces → necesario antes de implementar UI
3. Implementación de DAOs → base para lógica de negocio
4. Sistema de reservas con bloqueos → implementar y probar bien
5. Control de stock en pedidos → implementar y probar bien

### 🔴 Tareas de alto riesgo (dedicar más tiempo)

- Implementación de concurrencia en reservas: **+3h buffer**
- Control de stock atómico: **+2h buffer**
- Validación de solapamiento de sesiones: **+2h buffer**
- Sistema de encriptación: **+2h buffer**

---

## CONSEJOS PARA LA PLANIFICACIÓN EN PROJECTLIBRE

1. **Crear hitos** después de:
    
    - Análisis completado
    - Diseño completado
    - Implementación completada
    - Pruebas superadas
    - Proyecto entregado
2. **Tareas que pueden ir en paralelo**:
    
    - Diseño de BD y diseño de interfaces (parcial)
    - Implementación de módulos independientes
    - Documentación durante implementación (parcial)
3. **Buffer de tiempo**:
    
    - Añade 5-10% de buffer en tareas de riesgo alto
    - Deja margen para integración y ajustes finales
4. **Duración máxima por tarea individual**:
    
    - No más de 3-4 días laborables
    - Dividir tareas grandes en subtareas

---

## EJEMPLO DE CONVERSIÓN HORAS → DÍAS

**Asumiendo jornada de 8 horas**:

- 8 horas = 1 día
- 16 horas = 2 días
- 40 horas = 5 días (1 semana)
- 80 horas = 10 días (2 semanas)

**Para el proyecto de 3 meses**:

- 960 horas totales
- Con 1 persona a tiempo completo: 960h / 8h = 120 días = ~6 meses
- Con múltiples recursos y paralelización: 12 semanas (3 meses)
