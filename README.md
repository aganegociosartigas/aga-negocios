# AGA Negocios - Sistema de Administración

Sistema completo de e-commerce y administración para AGA Negocios.

## 🚀 Despliegue en Railway

### Paso 1: Crear cuenta en Railway
1. Ir a [railway.app](https://railway.app)
2. Crear cuenta con GitHub

### Paso 2: Crear nuevo proyecto
1. Clic en "New Project"
2. Seleccionar "Deploy from GitHub repo"
3. Conectar tu repositorio

### Paso 3: Configurar variables de entorno
En Railway, ir a "Variables" y agregar:

```
DATABASE_URL=file:/app/data/aga-negocios.db
NEXTAUTH_SECRET=tu-clave-secreta-muy-larga-y-aleatoria
NEXTAUTH_URL=https://tu-proyecto.railway.app
NODE_ENV=production
```

### Paso 4: Agregar volumen para persistir datos
1. Ir a "Volumes" en Railway
2. Clic en "New Volume"
3. Montar en: `/app/data`
4. Guardar cambios

### Paso 5: Desplegar
Railway detectará Next.js y desplegará automáticamente.

---

## 🔐 Credenciales del Admin

- **URL:** `tu-dominio.com/admin`
- **Email:** `admin@aganegocios.com`
- **Password:** `admin123`

⚠️ **Cambiar la contraseña después del primer login**

---

## 📁 Estructura del Proyecto

```
├── prisma/
│   └── schema.prisma     # Esquema de base de datos
├── src/
│   ├── app/
│   │   ├── admin/        # Panel de administración
│   │   ├── api/          # API Routes
│   │   └── page.tsx      # Landing page pública
│   └── components/       # Componentes React
├── railway.toml          # Configuración de Railway
└── package.json
```

---

## 🛠️ Comandos

```bash
# Desarrollo
bun run dev

# Build
bun run build

# Base de datos
bun run db:push
bun run db:generate
```

---

## 📋 Funcionalidades

### Panel Admin
- ✅ Dashboard con estadísticas
- ✅ Gestión de productos (CRUD)
- ✅ Gestión de contactos
- ✅ Newsletter con exportación CSV
- ✅ Creador de popups promocionales
- ✅ Gestión de remates
- ✅ Configuración SEO

### Landing Page
- ✅ Tienda online
- ✅ Productos destacados
- ✅ Integración WhatsApp
- ✅ Newsletter
- ✅ Formulario de contacto
- ✅ SEO optimizado

---

## 📧 Email Marketing

Exportá suscriptores desde `/admin` → Newsletter → Exportar CSV
Compatible con: Mailchimp, SendGrid, HubSpot

---

## 🤖 Posicionamiento en IA

El sitio está optimizado para aparecer en:
- ChatGPT
- Perplexity AI
- Claude
- Google AI Overview
