<!-- Copyright (c) 2025 Adrián Quiroga Linares Lectura y referencia permitidas; reutilización y plagio prohibidos -->

# ESPECIFICACIÓN DEL PROYECTO

## Sistema de Gestión de Cine "Ixildu, Hasiko da!"

---

## 1. ALCANCE DEL SISTEMA

### 1.1 Descripción General

Sistema de información integral para la gestión de un cine ubicado en Donosti (País Vasco, España). El sistema permite administrar todas las operaciones del cine incluyendo cartelera, reservas, restauración, recursos humanos e instalaciones.

### 1.2 Propósito

Proporcionar una plataforma completa que permita:

- **A los administradores**: gestionar todos los aspectos operativos del cine
- **A los clientes**: consultar cartelera, realizar reservas, pedir comida y valorar películas

### 1.3 Usuarios del Sistema

- **Administrador único**: Gestión completa del sistema (creado desde el gestor de BD)
- **Clientes**: Usuarios registrados que pueden reservar y utilizar servicios del cine

---

## 2. REQUISITOS FUNCIONALES

### 2.1 Módulo de Autenticación y Usuarios (3 transacciones)

**RF-01**: Autenticación de usuarios (admin/cliente) **RF-02**: Registro de nuevos clientes **RF-03**: Edición de datos personales del cliente **RF-04**: Eliminación de cuenta de cliente

### 2.2 Módulo de Gestión de Cartelera (8 transacciones)

**RF-05**: Búsqueda de películas con múltiples filtros **RF-06**: Inserción de nuevas películas **RF-07**: Actualización de datos de películas **RF-08**: Eliminación de películas **RF-09**: Creación de sesiones/emisiones **RF-10**: Modificación de sesiones **RF-11**: Eliminación de sesiones **RF-12**: Asignación/desasignación de anuncios a sesiones

### 2.3 Módulo de Reservas (5 transacciones)

**RF-13**: Consulta de sesiones disponibles (con filtros) **RF-14**: Consulta de disponibilidad de butacas en sala **RF-15**: Creación de reservas de butacas **RF-16**: Consulta de reservas activas del usuario **RF-17**: Cancelación de reservas activas

### 2.4 Módulo de Restauración (5 transacciones)

**RF-18**: Consulta de comidas disponibles **RF-19**: Creación de pedidos de comida **RF-20**: Consulta de pedidos activos **RF-21**: Cancelación de pedidos activos **RF-22**: Gestión de menú (añadir/eliminar comidas) - Admin

### 2.5 Módulo de Valoraciones (5 transacciones)

**RF-23**: Inserción de valoración de película **RF-24**: Edición de valoración propia **RF-25**: Eliminación de valoración propia **RF-26**: Consulta de valoraciones propias **RF-27**: Consulta de valoraciones de una película (con media)

### 2.6 Módulo de Recursos Humanos (6 transacciones)

**RF-28**: Inserción de trabajadores **RF-29**: Edición de datos de trabajadores **RF-30**: Eliminación de trabajadores **RF-31**: Búsqueda de trabajadores **RF-32**: Asignación de trabajadores a salas **RF-33**: Consulta de trabajadores por sala

### 2.7 Módulo de Instalaciones (5 transacciones)

**RF-34**: Consulta de equipamiento por sala **RF-35**: Inserción de equipo en sala **RF-36**: Edición de equipo **RF-37**: Eliminación de equipo **RF-38**: Consulta de información completa de sala

### 2.8 Módulo de Consultas de Información (2 transacciones)

**RF-39**: Consulta de información detallada de película **RF-40**: Consulta de información detallada de sala

**TOTAL: 40 transacciones funcionales**

---

## 3. REQUISITOS NO FUNCIONALES

### 3.1 Seguridad

**RNF-01**: Las contraseñas deben almacenarse encriptadas **RNF-02**: Validación de credenciales en cada acceso **RNF-03**: Diferenciación de permisos según tipo de usuario

### 3.2 Integridad de Datos

**RNF-04**: Control de concurrencia en reservas de butacas (SELECT FOR UPDATE) **RNF-05**: Control de concurrencia en pedidos de comida (SELECT FOR UPDATE) **RNF-06**: Validación de solapamiento de sesiones en salas **RNF-07**: Control de stock en pedidos de comida

### 3.3 Restricciones de Negocio

**RNF-08**: No permitir eliminar películas con sesiones asociadas **RNF-09**: No permitir eliminar sesiones con reservas (o reembolso previo) **RNF-10**: No permitir eliminar usuarios con reservas/pedidos/valoraciones activas **RNF-11**: No permitir reservar butacas ya ocupadas **RNF-12**: No permitir cancelar reservas de sesiones ya iniciadas **RNF-13**: No permitir pedidos superiores al stock disponible

### 3.4 Usabilidad

**RNF-14**: Interfaz gráfica intuitiva diferenciada para admin y clientes **RNF-15**: Visualización gráfica del plano de butacas **RNF-16**: Filtros de búsqueda en múltiples módulos **RNF-17**: Mensajes de error informativos

---

## 4. ESTRUCTURA DE DESGLOSE DEL TRABAJO (EDT)

### Nivel 1: PROYECTO SISTEMA GESTIÓN CINE

#### Nivel 2: COMPONENTES PRINCIPALES

##### 4.1 **MÓDULO DE AUTENTICACIÓN Y USUARIOS**

- 4.1.1 Sistema de login
- 4.1.2 Gestión de cuentas de cliente
- 4.1.3 Encriptación de contraseñas

##### 4.2 **MÓDULO DE GESTIÓN DE CARTELERA**

- 4.2.1 CRUD de películas
- 4.2.2 CRUD de sesiones
- 4.2.3 Gestión de anuncios
- 4.2.4 Control de solapamientos

##### 4.3 **MÓDULO DE RESERVAS**

- 4.3.1 Consulta de disponibilidad
- 4.3.2 Sistema de reservas con bloqueos
- 4.3.3 Visualización de butacas
- 4.3.4 Gestión de reservas activas

##### 4.4 **MÓDULO DE RESTAURACIÓN**

- 4.4.1 Catálogo de comidas
- 4.4.2 Sistema de pedidos con control de stock
- 4.4.3 Gestión de pedidos activos
- 4.4.4 Control de inventario

##### 4.5 **MÓDULO DE VALORACIONES**

- 4.5.1 Sistema de opiniones
- 4.5.2 Sistema de puntuaciones
- 4.5.3 Cálculo de medias
- 4.5.4 Gestión de valoraciones propias

##### 4.6 **MÓDULO DE RECURSOS HUMANOS**

- 4.6.1 Gestión de trabajadores proyección
- 4.6.2 Gestión de trabajadores limpieza
- 4.6.3 Asignación sala-trabajador
- 4.6.4 Consultas de personal

##### 4.7 **MÓDULO DE INSTALACIONES**

- 4.7.1 Gestión de salas
- 4.7.2 Gestión de equipamiento
- 4.7.3 Gestión de butacas
- 4.7.4 Consultas de infraestructura

##### 4.8 **BASE DE DATOS**

- 4.8.1 Modelo Entidad-Relación
- 4.8.2 Modelo Relacional (17 tablas)
- 4.8.3 Restricciones de integridad
- 4.8.4 Triggers y procedimientos

##### 4.9 **INTERFAZ DE USUARIO**

- 4.9.1 Interfaz de administración
    - Ventana principal con menú
    - Gestión de películas
    - Gestión de cartelera
    - Gestión de restauración
    - Gestión de RR.HH
    - Gestión de instalaciones
- 4.9.2 Interfaz de cliente
    - Autenticación y registro
    - Ventana principal con sesiones
    - Configuración de cuenta
    - Reservas y butacas
    - Pedidos de comida
    - Valoraciones

##### 4.10 **DOCUMENTACIÓN**

- 4.10.1 Manual de usuario (cliente)
- 4.10.2 Manual de administrador
- 4.10.3 Documentación técnica
- 4.10.4 Diccionario de datos

---

## 5. ENTIDADES PRINCIPALES DEL SISTEMA

### 5.1 Base de Datos (17 Tablas)

1. **Usuario** (cliente/admin)
2. **Película**
3. **Sesión**
4. **Sala**
5. **Butaca**
6. **Reserva**
7. **Anuncio**
8. **Anunciar** (relación sesión-anuncio)
9. **Comida**
10. **Pedir** (pedidos de comida)
11. **Valorar** (opiniones)
12. **TrabajadorProyección**
13. **TrabajadorLimpieza**
14. **TrabajarProyección** (asignación)
15. **TrabajarLimpieza** (asignación)
16. **Equipo**
17. **Butaca** (con estado de reserva)

---

## 6. RESTRICCIONES DEL PROYECTO

### 6.1 Técnicas

- Lenguaje: Java
- Base de datos: SQL (con gestor específico de BD)
- Encriptación de contraseñas obligatoria
- Control de concurrencia mediante SELECT FOR UPDATE

### 6.2 De Negocio

- Un único administrador del sistema
- Idioma por defecto: Vasco
- Precio base sesión: 7.50€
- Precio base reserva: 0.00€
- Sueldo base trabajador: 1000€
- Tipo usuario por defecto: "Normal"
- Tipo butaca por defecto: "Normal"

### 6.3 De Integridad Referencial

- Borrado en cascada para dependencias fuertes
- Borrado restringido para entidades principales
- Establecer NULL para relaciones opcionales

---

## 7. PRIORIZACIÓN DE FUNCIONALIDADES

### Prioridad CRÍTICA (MVP - Incremento 1)

- Autenticación básica
- Consulta de sesiones disponibles
- Reserva de butacas
- Gestión básica de películas (admin)
- Gestión básica de sesiones (admin)

### Prioridad ALTA (Incremento 2)

- Gestión completa de usuarios
- Pedidos de comida
- Valoraciones de películas
- Gestión de cartelera completa
- Gestión de anuncios

### Prioridad MEDIA (Incremento 3)

- Gestión de RR.HH
- Gestión de instalaciones
- Consultas avanzadas
- Informes y estadísticas

---

## 8. RIESGOS IDENTIFICADOS

### Riesgo ALTO

**R-01**: Condiciones de carrera en reservas simultáneas

- Mitigación: Bloqueos en dos fases (SELECT FOR UPDATE)

**R-02**: Sobreventas de comida (stock negativo)

- Mitigación: Validación atómica con bloqueos

**R-03**: Solapamiento de sesiones en salas

- Mitigación: Validación temporal antes de insertar/actualizar

### Riesgo MEDIO

**R-04**: Pérdida de integridad referencial

- Mitigación: Restricciones de FK bien definidas

**R-05**: Contraseñas en texto plano

- Mitigación: Encriptación obligatoria implementada

**R-06**: Eliminaciones accidentales con datos relacionados

- Mitigación: Validaciones previas y mensajes informativos

### Riesgo BAJO

**R-07**: Usabilidad compleja para usuarios finales

- Mitigación: Diseño de interfaces intuitivas

---

## 9. MÉTRICAS DEL PROYECTO

- **Entidades del modelo**: 17 tablas
- **Transacciones totales**: 40
- **Ventanas de interfaz**: 18 (aprox.)
- **Tipos de usuario**: 2 (admin, cliente)
- **Módulos funcionales**: 8
- **Relaciones entre tablas**: 13 claves externas

---

## 10. SUPUESTOS Y DEPENDENCIAS

### Supuestos

- El administrador se crea directamente en la BD (no hay registro de admin)
- Las películas tienen un trailer asociado
- Cada sala tiene un nombre y múltiples butacas
- Los anuncios tienen temática y duración
- Los trabajadores se dividen en dos tipos (proyección y limpieza)

### Dependencias

- Acceso a gestor de base de datos SQL
- Biblioteca de encriptación para contraseñas
- Entorno de desarrollo Java
- Sistema operativo compatible

---

## DIAGRAMA EDT (Vista de Árbol)

```
SISTEMA GESTIÓN CINE
│
├── 1. AUTENTICACIÓN Y USUARIOS
│   ├── Login
│   ├── Registro
│   └── Gestión cuenta
│
├── 2. CARTELERA
│   ├── Películas (CRUD)
│   ├── Sesiones (CRUD)
│   └── Anuncios
│
├── 3. RESERVAS
│   ├── Consulta disponibilidad
│   ├── Reserva butacas
│   └── Gestión reservas
│
├── 4. RESTAURACIÓN
│   ├── Catálogo comidas
│   ├── Pedidos
│   └── Control stock
│
├── 5. VALORACIONES
│   ├── Crear opiniones
│   ├── Editar/Eliminar
│   └── Consultar valoraciones
│
├── 6. RR.HH
│   ├── Trabajadores
│   └── Asignaciones
│
├── 7. INSTALACIONES
│   ├── Salas
│   ├── Equipamiento
│   └── Butacas
│
├── 8. BASE DE DATOS
│   ├── Modelo ER
│   ├── Modelo Relacional
│   └── Integridad
│
├── 9. INTERFACES
│   ├── UI Admin
│   └── UI Cliente
│
└── 10. DOCUMENTACIÓN
    ├── Manuales
    └── Técnica
```
