# Guía de instalación y configuración de Soundhire

Esta guía te ayudará a configurar el proyecto Soundhire en tu entorno local.

## Requisitos previos

1. **Node.js**: Versión 18 o superior
   - Descarga: [https://nodejs.org/](https://nodejs.org/)

2. **PostgreSQL**: Asegúrate de tener PostgreSQL instalado y en ejecución
   - Descarga: [https://www.postgresql.org/download/](https://www.postgresql.org/download/)

3. **Git**: Para clonar el repositorio
   - Descarga: [https://git-scm.com/downloads](https://git-scm.com/downloads)

## Pasos de instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/Ignacioaresc/soundhire-app.git
cd soundhire-app
```

### 2. Instalar dependencias

```bash
npm install
```

### 3. Configurar la base de datos

Crea una base de datos PostgreSQL para el proyecto:

```sql
CREATE DATABASE soundhire;
```

### 4. Configurar variables de entorno

Crea un archivo `.env` en la raíz del proyecto con el siguiente contenido (ajusta según tu configuración):

```
DATABASE_URL=postgresql://usuario:contraseña@localhost:5432/soundhire
NODE_ENV=development
PORT=5000
SESSION_SECRET=algun_secreto_seguro
```

### 5. Inicializar la base de datos

Ejecuta las migraciones para crear las tablas en la base de datos:

```bash
npm run db:push
```

### 6. Inicializar datos básicos (opcional)

Para crear datos de prueba y configuraciones iniciales:

```bash
npm run init:settings
npm run add:testusers
```

### 7. Iniciar el servidor de desarrollo

```bash
npm run dev
```

La aplicación estará disponible en: http://localhost:5000

## Estructura de usuarios de prueba

Si has ejecutado el script de usuarios de prueba, puedes acceder con las siguientes credenciales:

- **DJ**:
  - Usuario: dj@test.com
  - Contraseña: password123

- **Cliente**:
  - Usuario: client@test.com
  - Contraseña: password123

- **Club**:
  - Usuario: club@test.com
  - Contraseña: password123

- **Administrador**:
  - Usuario: admin@test.com
  - Contraseña: password123

## Solución de problemas comunes

### Error de conexión a la base de datos
- Verifica que PostgreSQL esté en ejecución
- Comprueba que la URL de conexión en el archivo `.env` sea correcta
- Asegúrate de que el usuario tenga permisos para acceder a la base de datos

### Problemas con dependencias
Si tienes problemas con las dependencias, intenta:
```bash
rm -rf node_modules
npm cache clean --force
npm install
```

### Errores al iniciar el servidor
- Verifica que el puerto especificado (por defecto 5000) no esté en uso
- Asegúrate de tener todos los permisos necesarios para las carpetas de uploads