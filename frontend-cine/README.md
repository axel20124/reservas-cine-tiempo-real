# Frontend - Puesta en marcha

## Requisitos previos

- Node.js instalado.
- npm instalado.
- API Gateway y servicios backend configurados y funcionando.

## 1. Instalación

Desde la carpeta `frontend-cine`, ejecutar:

```bash
npm install express
```

## 2. Iniciar el frontend

Desde la carpeta `frontend-cine`, ejecutar:

```bash
node server.js
```

Si se inicia correctamente, aparecerá:

```text
Frontend disponible en http://localhost:3000
```

## 3. Acceder desde el navegador

**Modo WebSocket:**

http://localhost:3000

**Modo Polling:**

http://localhost:3000/polling.html

## 4. Generar un token JWT

Desde la carpeta principal del proyecto (`Cine`), ejecutar:

```bash
npm run token:asientos -- ana (ejemplo establecido en asientos)
```

Copiar el token generado y pegarlo en el campo de autenticación del frontend.

## 5. Comandos útiles

Ejecutar desde la carpeta principal `Cine`:

| Comando | Función |
|---|---|
| `npm install` | Instalar dependencias de los workspaces |
| `npm run dev:funciones` | Iniciar servicio de Funciones |
| `npm run dev:asientos` | Iniciar servicio de Asientos |
| `npm run db:init:funciones` | Inicializar base de datos de Funciones |
| `npm run db:init:asientos` | Inicializar base de datos de Asientos |
| `npm run token:asientos -- ana` | Generar token JWT |
| `npm run start:funciones` | Iniciar Funciones sin modo desarrollo |
| `npm run start:asientos` | Iniciar Asientos sin modo desarrollo |

Para ejecutar el frontend:

```bash
cd frontend-cine
node server.js
```

## 6. Puertos utilizados

| Servicio | Puerto |
|---|---:|
| Frontend | 3000 |
| Servicio de Asientos | 3001 |
| Servicio de Funciones | 3002 |
| API Gateway | 8080 |

**Importante:** mantener abiertos los terminales de los servicios backend, el Gateway y el frontend mientras se utiliza la aplicación.

