# Soundhire - Plataforma para DJs

Soundhire es una aplicación web completa para la contratación y gestión de DJs. Está diseñada para conectar DJs con clientes, clubs y empresas de eventos, facilitando la reserva de servicios, gestión de disponibilidad y seguimiento de eventos.

## Características principales

- **Gestión de perfil de DJ**: Los DJs pueden crear y gestionar perfiles profesionales detallados.
- **Sistema de disponibilidad**: Calendario interactivo para que los DJs marquen su disponibilidad.
- **Reservas de eventos**: Interfaz intuitiva para solicitar y gestionar reservas de actuaciones.
- **Panel de control personalizado**: Dashboard con información relevante para cada tipo de usuario.
- **Marketplace**: Espacio para ofrecer servicios y equipos de DJ.
- **Documentación financiera**: Gestión de contratos, facturas y transacciones.

## Tecnologías utilizadas

- **Frontend**: React, TypeScript, TailwindCSS, Shadcn/UI
- **Backend**: Node.js, Express
- **Base de datos**: PostgreSQL con Drizzle ORM
- **Estado y peticiones**: React Query
- **Calendario**: FullCalendar
- **Autenticación**: Passport.js

## Requisitos

- Node.js 18+
- PostgreSQL
- npm o yarn

## Instalación

1. Clona el repositorio:
   ```
   git clone https://github.com/Ignacioaresc/soundhire-app.git
   cd soundhire-app
   ```

2. Instala las dependencias:
   ```
   npm install
   ```

3. Configura la base de datos PostgreSQL.

4. Ejecuta las migraciones de la base de datos:
   ```
   npm run db:push
   ```

5. Inicia el servidor de desarrollo:
   ```
   npm run dev
   ```

## Estructura del proyecto

- `/client`: Código del frontend React
  - `/src/components`: Componentes reutilizables
  - `/src/pages`: Páginas de la aplicación
  - `/src/hooks`: Hooks personalizados
- `/server`: API backend y lógica de servidor
- `/db`: Esquemas de la base de datos y migraciones
- `/uploads`: Archivos subidos por los usuarios
- `/public`: Archivos estáticos

## Contribuir

1. Haz fork del proyecto
2. Crea una rama para tu funcionalidad (`git checkout -b feature/amazing-feature`)
3. Haz commit de tus cambios (`git commit -m 'Add some amazing feature'`)
4. Push a la rama (`git push origin feature/amazing-feature`)
5. Abre un Pull Request

## Licencia

Este proyecto está bajo la Licencia MIT.