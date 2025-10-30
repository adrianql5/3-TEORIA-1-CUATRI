 Plataforma web que conecta estudiantes universitarios para facilitar la tutoría entre pares y el intercambio de recursos académicos.

## 🚀 Stack Tecnológico

### Frontend
- Next.js 15 (App Router)
- TypeScript
- Tailwind CSS
- Socket.io-client (chat en tiempo real)
- Zustand (state management)

### Backend
- Node.js + Express
- TypeScript
- PostgreSQL (con pg/node-postgres)
- Socket.io (WebSockets)
- JWT (autenticación)

## 📋 Requisitos Previos

- Node.js 18+ y npm/yarn
- PostgreSQL 14+

## 🔧 Instalación

### 1. Clonar el repositorio
```bash
git clone <repository-url>
cd Xuntos
```

### 2. Configurar Backend

```bash
cd backend
npm install

# Copiar variables de entorno
cp .env.example .env

# Editar .env con tus credenciales de PostgreSQL
# DATABASE_URL="postgresql://postgres:tu_password@localhost:5432/xuntos"

# Iniciar servidor de desarrollo
# La base de datos y tablas se crearán automáticamente
npm run dev
```

El backend estará disponible en `http://localhost:5000`

**Nota:** El backend crea automáticamente la base de datos y todas las tablas al iniciarse por primera vez.

### 3. Configurar Frontend

```bash
cd frontend
npm install

# Copiar variables de entorno
cp .env.example .env.local

# Iniciar servidor de desarrollo
npm run dev
```

El frontend estará disponible en `http://localhost:3000`

## 📁 Estructura del Proyecto

```
/Xuntos
├── /frontend          # Aplicación Next.js
│   ├── /src
│   │   ├── /app       # App Router (rutas)
│   │   ├── /components
│   │   ├── /lib       # Utilidades y configuración
│   │   ├── /hooks
│   │   └── /types
│   └── package.json
│
├── /backend           # API Express
│   ├── /src
│   │   ├── /controllers
│   │   ├── /routes
│   │   ├── /middleware
│   │   ├── /services
│   │   ├── /utils
│   │   └── /prisma
│   ├── /uploads       # Archivos subidos (apuntes)
│   └── package.json
│
└── README.md
```

## 🎯 Funcionalidades Principales

- ✅ Sistema de autenticación con JWT
- ✅ Perfiles de usuario configurables
- ✅ Búsqueda avanzada de tutores
- ✅ Sistema de mensajería en tiempo real
- ✅ Gestión y compartición de apuntes
- ✅ Sistema de valoraciones y reseñas
- ✅ Diseño responsive

## 🗄️ Modelo de Base de Datos

### Tablas principales:
- **users**: Información de usuarios y autenticación
- **universities**: Catálogo de universidades
- **subjects**: Asignaturas disponibles
- **user_subjects**: Relación entre usuarios y asignaturas que imparten
- **notes**: Apuntes subidos por usuarios
- **conversations**: Conversaciones de chat
- **messages**: Mensajes de chat
- **reviews**: Valoraciones de tutores

## 🔐 Variables de Entorno

### Backend (.env)
```
DATABASE_URL="postgresql://user:password@localhost:5432/xuntos"
JWT_SECRET="your-secret-key"
PORT=5000
NODE_ENV=development
UPLOAD_DIR=./uploads
```

### Frontend (.env.local)
```
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXT_PUBLIC_SOCKET_URL=http://localhost:5000
```

## 📝 Scripts Disponibles

### Backend
- `npm run dev` - Iniciar servidor de desarrollo con hot reload
- `npm run build` - Compilar TypeScript a JavaScript
- `npm start` - Iniciar servidor de producción

**Gestión de Base de Datos:**
```bash
# Ver tablas de la base de datos
psql -U postgres -d xuntos -c "\dt"

# Ver datos de una tabla
psql -U postgres -d xuntos -c "SELECT * FROM users;"

# Resetear base de datos
psql -U postgres -c "DROP DATABASE xuntos;"
# Luego reinicia el backend para recrearla
```

### Frontend
- `npm run dev` - Iniciar Next.js en modo desarrollo
- `npm run build` - Crear build de producción
- `npm start` - Iniciar servidor de producción
- `npm run lint` - Ejecutar linter

## 🧪 Testing

```bash
# Backend
cd backend
npm test

# Frontend
cd frontend
npm test
```

## 📚 API Endpoints

### Autenticación
- `POST /api/auth/register` - Registro de usuario
- `POST /api/auth/login` - Inicio de sesión
- `GET /api/auth/me` - Obtener usuario actual

### Usuarios
- `GET /api/users` - Listar usuarios (con filtros)
- `GET /api/users/:id` - Obtener perfil de usuario
- `PUT /api/users/:id` - Actualizar perfil
- `GET /api/users/:id/notes` - Obtener apuntes de un usuario

### Asignaturas
- `GET /api/subjects` - Listar asignaturas
- `POST /api/subjects` - Crear asignatura (admin)

### Apuntes
- `POST /api/notes` - Subir apunte
- `GET /api/notes/:id` - Obtener apunte
- `DELETE /api/notes/:id` - Eliminar apunte
- `GET /api/notes/:id/download` - Descargar archivo

### Chat
- `GET /api/conversations` - Listar conversaciones del usuario
- `GET /api/conversations/:id/messages` - Obtener mensajes
- WebSocket events: `send_message`, `message_received`, `typing`

### Valoraciones
- `POST /api/reviews` - Crear valoración
- `GET /api/users/:id/reviews` - Obtener valoraciones de un tutor

## 🚀 Despliegue

### Backend
Se puede desplegar en:
- Railway
- Render
- Heroku
- VPS con PM2

### Frontend
Se puede desplegar en:
- Vercel (recomendado para Next.js)
- Netlify
- AWS Amplify

### Base de Datos
- PostgreSQL en Railway, Supabase o Render

## 🤝 Contribución

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -m 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT.

## 👥 Autores

- Tu Nombre - Desarrollo inicial

## 🙏 Agradecimientos

- A todos los estudiantes que inspiraron este proyecto
- Comunidad de código abierto