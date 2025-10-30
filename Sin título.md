# 📚 Xuntos - Plataforma de Colaboración entre Estudantes

## Descrición

**Xuntos** é unha aplicación web completamente en galego que permite a estudantes compartir perfís, apuntes e chatear entre eles. Agora con arquitectura cliente-servidor completa para persistencia de datos e comunicación en tempo real.

## Características Principais

✅ **Xestión de Perfís**
- Crear e editar o teu perfil persoal
- Descrición sobre ti e os teus estudos
- Lista de asignaturas que dominas
- Subir apuntes (texto ou arquivos)

✅ **Explorar Outros Usuarios**
- Ver lista de todos os usuarios rexistrados
- Consultar perfís doutros estudantes
- Ver os seus apuntes e asignaturas

✅ **Sistema de Chat**
- Iniciar conversas privadas con calquera usuario
- Historial de mensaxes
- Interface intuitiva estilo WhatsApp

✅ **Interface en Galego**
- Toda a aplicación está completamente en galego
- Deseño moderno e responsive (adaptado a móbil e escritorio)

✅ **Arquitectura Cliente-Servidor**
- Backend con Node.js e Express
- API REST para todas as operacións
- Persistencia de datos no servidor
- Comunicación asíncrona cliente-servidor

## Datos Iniciais de Demostración

A aplicación ven cargada con 5 usuarios de exemplo con perfís completos:

1. **María González** - Enxeñería Informática (con apuntes de JavaScript e SQL)
2. **Carlos Pérez** - Matemáticas (con apuntes de Estatística e Álxebra)
3. **Laura Fernández** - Física (con apuntes de Leis de Newton e Termodinámica)
4. **David Silva** - Filosofía e Literatura Galega (con apuntes de Filosofía)
5. **Ana Martínez** - Bioloxía (con apuntes de Fotosíntese e Ecosistemas)

Tamén inclúe conversas de exemplo entre os usuarios para demostrar o sistema de mensaxería.

## Requisitos

- **Node.js** (versión 14 ou superior)
- Navegador web moderno (Chrome, Firefox, Safari, Edge)

## Instalación e Uso

### Opción 1: Script Automático (Linux/macOS)

```bash
# 1. Darlle permisos de execución ao script (xa feito)
chmod +x iniciar.sh

# 2. Executar o script
./iniciar.sh
```

### Opción 2: Instalación Manual

```bash
# 1. Instalar dependencias do servidor
cd servidor
npm install

# 2. Iniciar o servidor
node server.js
```

### Opción 3: Usando npm desde a raíz

```bash
# 1. Instalar dependencias
npm run install-servidor

# 2. Iniciar a aplicación
npm run iniciar
```

## Acceder á Aplicación

Unha vez que o servidor estea en execución, verás unha mensaxe como esta:

```
🚀 Servidor Xuntos escoitando no porto 3000
📡 API dispoñible en http://localhost:3000/api
🌐 Cliente dispoñible en http://localhost:3000

✅ Datos iniciais cargados:
   👥 5 usuarios
   💬 18 mensaxes
   📚 9 apuntes totais
```

Abre o teu navegador e vai a: **http://localhost:3000**

## Como Usar

### 1. Seleccionar ou Crear Usuario

Ao abrir a aplicación, verás unha pantalla de benvida onde podes:
- **Seleccionar un usuario existente** (María, Carlos, Laura, David ou Ana)
- **Crear un novo usuario** escribindo o teu nome

### 2. Explorar a Aplicación

Unha vez dentro, tes acceso a tres seccións principais:

#### 📋 Usuarios
- Lista todos os usuarios rexistrados na plataforma
- Fai clic nun usuario para ver o seu perfil completo
- Desde o perfil dun usuario podes iniciar un chat con el/ela

#### 👤 O meu perfil
- Visualiza e edita o teu perfil
- Fai clic en "✏️ Editar perfil" para:
  - Modificar a túa descrición
  - Engadir ou eliminar asignaturas
  - Subir apuntes (texto ou arquivos)
- Non esquezas gardar os cambios!

#### 💬 Conversas
- Mostra todas as túas conversas activas
- Fai clic nunha conversa para seguir chateando

### 3. Funcionalidades Específicas

#### Engadir Asignaturas
1. Vai a "O meu perfil" → "Editar perfil"
2. Escribe o nome da asignatura no campo
3. Fai clic en "+ Engadir"
4. Podes eliminar asignaturas facendo clic no × de cada unha

#### Subir Apuntes
1. Vai a "O meu perfil" → "Editar perfil"
2. Escribe o nome do apunte
3. Elixe entre:
   - **+ Texto**: Escribe directamente o contido
   - **📎 Arquivo**: Sube un arquivo desde o teu ordenador (PDF, TXT, DOC, etc.)
4. Os apuntes de texto móstranse nun modal ao facer clic en "Ver"
5. Os arquivos descárganse ao facer clic en "Descargar"

#### Chatear con Usuarios
1. Vai a "Usuarios" e selecciona un usuario
2. Fai clic en "💬 Chatear" no seu perfil
3. Escribe mensaxes e pulsa "Enviar" ou Enter
4. As túas mensaxes aparecen á dereita en azul
5. As mensaxes do outro usuario aparecen á esquerda en branco

## Tecnoloxías Utilizadas

### Backend
- **Node.js**: Plataforma de execución
- **Express**: Framework web
- **CORS**: Middleware para permitir peticións cross-origin

### Frontend
- **HTML5**: Estrutura da aplicación
- **CSS3**: Estilos modernos e responsive
- **JavaScript Puro (ES6+)**: Toda a lóxica sen frameworks
- **Fetch API**: Comunicación asíncrona co servidor

## Estrutura de Arquivos

```
Proyecto/
├── cliente/                # Aplicación frontend
│   ├── index.html         # Estrutura principal
│   ├── styles.css         # Estilos e deseño
│   └── app.js             # Lóxica do cliente e API calls
├── servidor/              # Aplicación backend
│   ├── server.js          # Servidor Express e API REST
│   ├── datos.js           # Datos iniciais de demostración
│   └── package.json       # Dependencias do servidor
├── package.json           # Scripts principais
├── iniciar.sh             # Script de inicio automático
├── README.md              # Esta documentación
└── CLAUDE.md              # Guía para desenvolvemento
```

## API REST

O servidor expón os seguintes endpoints:

### Usuarios
- `GET /api/usuarios` - Obter todos os usuarios
- `GET /api/usuarios/:id` - Obter un usuario por ID
- `POST /api/usuarios` - Crear un novo usuario
- `PUT /api/usuarios/:id` - Actualizar un usuario

### Apuntes
- `GET /api/usuarios/:id/apuntes` - Obter apuntes dun usuario
- `POST /api/usuarios/:id/apuntes` - Engadir un apunte
- `DELETE /api/usuarios/:userId/apuntes/:apunteId` - Eliminar un apunte

### Mensaxes
- `GET /api/mensaxes` - Obter todas as mensaxes
- `GET /api/mensaxes/:usuario1Id/:usuario2Id` - Obter mensaxes entre dous usuarios
- `GET /api/usuarios/:id/conversas` - Obter conversas dun usuario
- `POST /api/mensaxes` - Enviar unha nova mensaxe

## Navegadores Soportados

✅ Chrome/Edge (versión recente)
✅ Firefox (versión recente)
✅ Safari (versión recente)
✅ Opera (versión recente)

## Limitacións Actuais

⚠️ **Importante**:
- Os datos gárdanse en memoria do servidor (pérdense ao reiniciar)
- Non hai autenticación real nin seguridade
- Non hai validación exhaustiva de datos
- Para produción, sería necesario unha base de datos real (MongoDB, PostgreSQL, etc.)

## Melloras Futuras (Ideas)

- 💾 Base de datos persistente (MongoDB/PostgreSQL)
- 🔐 Sistema de autenticación con JWT
- 🔒 Seguridade e validación de datos
- 🖼️ Subir imaxes de perfil
- 📱 Notificacións push de mensaxes novas
- 🔍 Buscador de usuarios e asignaturas
- 🏷️ Etiquetas e filtros para asignaturas
- ⭐ Sistema de valoracións de apuntes
- 📊 Panel de estatísticas
- 🌐 Despregue en produción (Heroku, Vercel, etc.)

## Solución de Problemas

### O servidor non inicia
- Verifica que tes Node.js instalado: `node --version`
- Asegúrate de que o porto 3000 non está en uso
- Instala as dependencias: `npm run install-servidor`

### Erro de conexión no cliente
- Verifica que o servidor está en execución
- Comproba a consola do navegador para erros
- Asegúrate de que o servidor está en http://localhost:3000

### Non aparecen os datos iniciais
- Reinicia o servidor
- Verifica que o arquivo `servidor/datos.js` existe
- Comproba a consola do servidor para erros

## Licenza

Este proxecto é software libre de uso educativo.

---

Desenvolvido con ❤️ para a comunidade estudantil galega.