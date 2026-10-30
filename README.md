# 🐳 Next.js Docker App

Aplicación Next.js y TypeScript contenerizada con Docker para un entorno portable y consistente.

## Tecnologías

- Next.js 16 y React
- TypeScript
- Node.js 22 Alpine
- Docker

## Requisitos

Docker Desktop instalado y en funcionamiento.

## Construir la imagen

```bash
docker build -t nextjs-docker-app .
```

## Ejecutar el contenedor

```bash
docker run --rm -d -p 3000:3000 --name nextjs-docker-container nextjs-docker-app
```

Abrir http://localhost:3000

## Verificar y detener

```bash
docker ps
docker logs nextjs-docker-container
docker stop nextjs-docker-container
```

## Configuración

- `Dockerfile`: construcción en tres etapas (dependencias, compilación y producción).
- `.dockerignore`: excluye `node_modules`, `.next`, `.env` y archivos innecesarios.

## Resultado

La imagen se construyó correctamente y Next.js 16.4.3 inició en el puerto 3000 sin errores.