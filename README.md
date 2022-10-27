# Strapi + N8N

## Despliegue de stack

- Instalar Strapi
  **"npx create-strapi-app@latest app"**
- Copiar **Dockerfile** y **.dockerignore** a **"./app"** (carpeta del proyecto de Strapi)

## Creacion de contenedores

- Ejecutar **"docker-compose up -d"**
  > Se crean 4 contenedores:
  > strapi
  > strapi_db (postgres)
  > n8n
  > n8n_db (postgres)

Tener en cuenta los valores de las variables de entorno con respecto a los nombres de los servicios.

## Entorno desarrollo Strapi

Para poder utilizar el modo desarrollo, es necesario abrir el puerto de strapi_db.

- Ejecutar **"docker-compose -f docker-compose.yml -f docker-compose.dev.yml up -d strapi_db"**

- y localmente desde ./app ejecutar **"npm run develop"**

  > El modo desarrollo se abre en el puerto indicado en ./app/.env (variables de entorno de Strapi)

## Pendiente

- [] Las imagenes se guardan en ./app/public/upload. Se debería configuar cloudinary o algo similar.
