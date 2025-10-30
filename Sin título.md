# 📚 Xuntos - Plataforma de Colaboración entre Estudantes

## Descrición

**Xuntos** é unha aplicación web completamente en galego que permite a estudantes compartir perfís, apuntes e chatear entre eles. Agora con **autenticación segura** y **base de datos PostgreSQL** para persistencia completa de datos.

## ✨ Características Principais

✅ **Sistema de Autenticación**
- Rexistro de novos usuarios con email e contraseña
- Login seguro con JWT (JSON Web Tokens)
- Contraseñas hasheadas con bcrypt
- Sesión persistente (token válido 7 días)
- Soporte para múltiples sesións simultáneas

✅ **Xestión de Perfís**
- Crear e editar o teu perfil persoal
- **Foto de perfil personalizada** (sube imaxes ata 2MB)
- Descrición sobre ti e os teus estudos
- Lista de asignaturas que dominas
- Subir apuntes (texto ou arquivos)

✅ **Interface Personalizable**
- **Modo claro e modo oscuro** con toggle
- Preferencias gardadas automaticamente
- Deseño responsive e moderno

✅ **Explorar Outros Usuarios**
- Ver lista de todos os usuarios rexistrados
- Consultar perfís doutros estudantes
- Ver os seus apuntes e asignaturas

✅ **Sistema de Chat**
- Iniciar conversas privadas con calquera usuario
- Historial de mensaxes persistente
- Interface intuitiva estilo WhatsApp

✅ **Base de Datos PostgreSQL**
- Persistencia completa de todos os datos
- Esquema relacional optimizado
- Queries eficientes con índices

## 🗄️ Datos Iniciais de Demostración

A aplicación ven cargada con 5 usuarios de exemplo con perfís completos:

| Email | Contraseña | Nome | Area |
|-------|------------|------|------|
| maria@xuntos.gal | demo123 | María González | Enxeñería Informática |
| carlos@xuntos.gal | demo123 | Carlos Pérez | Matemáticas |
| laura@xuntos.gal | demo123 | Laura Fernández | Física |
| david@xuntos.gal | demo123 | David Silva | Filosofía |
| ana@xuntos.gal | demo123 | Ana Martínez | Bioloxía |

Cada usuario ten apuntes completos nas súas respectivas materias. Tamén hai 18 mensaxes de conversa entre os usuarios para demostrar o sistema de chat.

## 📋 Requisitos

- **Node.js** (versión 14 ou superior)
- **PostgreSQL** (versión 12 ou superior)
- Navegador web moderno (Chrome, Firefox, Safari, Edge)

## 🔧 Instalación

### 1. Instalar PostgreSQL

#### Ubuntu/Debian:
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo systemctl start postgresql
sudo systemctl enable postgresql
```

#### macOS (con Homebrew):
```bash
brew install postgresql@15
brew services start postgresql@15
```

#### Windows:
Descarga desde: https://www.postgresql.org/download/windows/

### 2. Configurar PostgreSQL

```bash
# Acceder a PostgreSQL
sudo -u postgres psql

# Cambiar contraseña do usuario postgres
ALTER USER postgres WITH PASSWORD 'postgres';

# Sair
\q
```

### 3. Instalar Dependencias

```bash
cd servidor
npm install
```

### 4. Inicializar a Base de Datos

**Se é a primeira vez:**
```bash
cd servidor
npm run init-db
```

Este comando:
- Crea o usuario `xuntos_user` en PostgreSQL
- Crea a base de datos `xuntos_db`
- Xera todas as tablas (usuarios, asignaturas, apuntes, mensaxes)
- Insire os datos de demostración (5 usuarios con perfís e fotos)

**Se xa tes a base de datos e queres engadir soporte para fotos:**
```bash
cd servidor
npm run migrate
```

Se tes outra contraseña de postgres:
```bash
node init-db.js --postgres-password TUA_CONTRASEÑA
```

Para recrear a BD desde cero:
```bash
npm run reset-db
```

### 5. Iniciar o Servidor

```bash
cd servidor
npm start
```

Deberías ver:
```
==========================================
   🚀 SERVIDOR XUNTOS
==========================================

📡 Servidor escoitando no porto 3000
🌐 Cliente: http://localhost:3000
📡 API: http://localhost:3000/api

✅ Conexión á base de datos PostgreSQL establecida

📊 Datos na base de datos:
   👥 5 usuarios
   📚 9 apuntes
   💬 18 mensaxes

🔐 Credenciais de acceso:
   Email: maria@xuntos.gal
   Contraseña: demo123

==========================================
```

### 6. Acceder á Aplicación

Abre o navegador en: **http://localhost:3000**

**Para usar múltiples sesións na mesma máquina:**
- Abre varias ventás ou pestanas do navegador
- Cada unha pode iniciar sesión con un usuario diferente
- As sesións son independentes grazas aos JWT
- Proba iniciar sesión como `maria@xuntos.gal` nunha ventá e como `carlos@xuntos.gal` noutra para chatear entre eles!

## 🔐 Como Usar

### Primeira Vez

1. **Login con usuario de demostración:**
   - Email: `maria@xuntos.gal`
   - Contraseña: `demo123`

2. **Ou crear unha nova conta:**
   - Fai clic en "Rexístrate aquí"
   - Introduce o teu nome, email e contraseña (mínimo 6 caracteres)
   - A túa conta será creada automaticamente

### Funcionalidades

#### 📋 Explorar Usuarios
- Ve á sección "Usuarios" no menú superior
- Fai clic nun usuario para ver o seu perfil completo
- Desde o perfil, podes ver os seus apuntes e iniciar un chat

#### 👤 O Meu Perfil
- Fai clic en "O meu perfil" no menú
- **Cambiar foto de perfil:** Fai clic en "📷 Cambiar foto" e selecciona unha imaxe
- Edita a túa descrición e asignaturas
- Engade apuntes (texto ou arquivos PDF/DOC)
- Todos os cambios gárdanse na base de datos

#### 🌙 Modo Claro/Oscuro
- Fai clic no botón 🌙/☀️ na cabeceira
- A túa preferencia gárdase automaticamente
- Funciona en todas as vistas da aplicación

#### 💬 Chatear
- Desde o perfil dun usuario, fai clic en "💬 Chatear"
- Escribe mensaxes e pulsa Enter ou "Enviar"
- Todas as conversas persisten na base de datos
- Accede ás túas conversas desde "Conversas" no menú

#### 🚪 Pechar Sesión
- Fai clic en "🚪 Pechar sesión" na cabeceira
- O token será eliminado e volverás ao login

## 🏗️ Arquitectura Técnica

### Backend

- **Node.js** con Express
- **PostgreSQL** para persistencia
- **bcrypt** para hash de contraseñas (10 rounds)
- **JWT** para autenticación (7 días de validez)
- **CORS** habilitado para desarrollo

### Frontend

- HTML5 con vistas dinámicas
- CSS3 responsive
- JavaScript puro (ES6+) con async/await
- LocalStorage para almacenar JWT
- Fetch API para comunicación con servidor

### Base de Datos

**Tablas:**
- `usuarios` - Perfís de usuarios
- `usuario_asignaturas` - Asignaturas por usuario
- `apuntes` - Notas e arquivos
- `mensaxes` - Chat entre usuarios

**Seguridade:**
- Contraseñas hasheadas con bcrypt (nunca en texto plano)
- Autenticación JWT en todas as rutas protexidas
- Validación de permisos (só podes editar o teu propio perfil)

## 📡 API REST

### Autenticación
- `POST /api/auth/registro` - Rexistrar novo usuario
- `POST /api/auth/login` - Iniciar sesión
- `GET /api/auth/me` - Obter usuario actual (require token)

### Usuarios
- `GET /api/usuarios` - Listar usuarios (require token)
- `GET /api/usuarios/:id` - Obter usuario por ID
- `PUT /api/usuarios/:id` - Actualizar perfil

### Apuntes
- `GET /api/usuarios/:id/apuntes` - Listar apuntes
- `POST /api/usuarios/:id/apuntes` - Crear apunte
- `DELETE /api/usuarios/:userId/apuntes/:apunteId` - Eliminar apunte

### Mensaxes
- `GET /api/mensaxes/:usuario1Id/:usuario2Id` - Conversación
- `GET /api/usuarios/:id/conversas` - Listar conversas
- `POST /api/mensaxes` - Enviar mensaxe

## 🔍 Verificar a Instalación

### Comprobar PostgreSQL
```bash
sudo systemctl status postgresql
```

### Conectar á base de datos
```bash
psql -h localhost -U xuntos_user -d xuntos_db
# Contraseña: xuntos_password
```

### Ver usuarios na BD
```sql
SELECT id, nome, email FROM usuarios;
```

### Ver estatísticas
```sql
SELECT
    (SELECT COUNT(*) FROM usuarios) as usuarios,
    (SELECT COUNT(*) FROM apuntes) as apuntes,
    (SELECT COUNT(*) FROM mensaxes) as mensaxes;
```

## 🛠️ Comandos Útiles

```bash
# Iniciar servidor
cd servidor && npm start

# Reiniciar base de datos
cd servidor && npm run reset-db

# Ver logs do servidor
# (Os logs aparecen na consola onde executaches npm start)

# Backup da base de datos
pg_dump -h localhost -U xuntos_user xuntos_db > backup.sql

# Restaurar backup
psql -h localhost -U xuntos_user xuntos_db < backup.sql
```

## ⚠️ Solución de Problemas

### PostgreSQL non se conecta
```bash
# Verificar que está en execución
sudo systemctl status postgresql

# Reiniciar
sudo systemctl restart postgresql
```

### Erro "peer authentication failed"
Edita `/etc/postgresql/*/main/pg_hba.conf`:
```
# Cambia:
local   all             all                                     peer

# Por:
local   all             all                                     md5
```

Reinicia:
```bash
sudo systemctl restart postgresql
```

### Porto 3000 en uso
Cambia o porto en `.env`:
```
PORT=3001
```

### Erro de conexión no cliente
1. Verifica que o servidor está activo
2. Abre a consola do navegador (F12)
3. Verifica a URL da API en `cliente/app.js`

## 📊 Estrutura do Proxecto

```
Proyecto/
├── cliente/                   # Aplicación frontend
│   ├── index.html            # HTML con vistas de login/app
│   ├── app.js                # Cliente con autenticación JWT
│   └── styles.css            # Estilos responsive
├── servidor/                  # Aplicación backend
│   ├── server.js             # Servidor Express con auth
│   ├── database.js           # Capa de acceso a datos
│   ├── schema.sql            # Esquema de tablas PostgreSQL
│   ├── seed.sql              # Datos iniciais
│   ├── init-db.js            # Script de inicialización
│   ├── .env                  # Configuración
│   └── package.json          # Dependencias
├── INSTALACION.md            # Guía detallada de instalación
├── README.md                 # Esta documentación
└── CLAUDE.md                 # Guía para desenvolvemento
```

## 🔒 Seguridade

- ✅ Contraseñas hasheadas con bcrypt
- ✅ Tokens JWT con expiración
- ✅ Validación de permisos por usuario
- ✅ CORS configurado
- ✅ SQL injection prevention (prepared statements)
- ⚠️ Para produción, cambia `JWT_SECRET` en `.env`

## 🚀 Próximas Melloras

- [ ] WebSocket para chat en tempo real
- [ ] Notificacións push
- [ ] Búsqueda de usuarios e apuntes
- [ ] Sistema de grupos
- [ ] Compartir apuntes entre usuarios
- [ ] Panel de administración
- [ ] Tests automatizados
- [ ] Deploy en produción (Heroku, Vercel)

## 💡 Notas Importantes

- Os datos persisten en PostgreSQL localmente
- As contraseñas están hasheadas (non se poden recuperar)
- Os tokens JWT caducan aos 7 días
- O servidor usa porto 3000 por defecto
- PostgreSQL usa porto 5432 por defecto

## 📄 Licenza

Este proxecto é software libre de uso educativo.

---

**¿Problemas?** Revisa `INSTALACION.md` para unha guía detallada paso a paso.

Desenvolvido con ❤️ para a comunidade estudantil galega.