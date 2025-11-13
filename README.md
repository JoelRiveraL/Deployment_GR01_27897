# Deployment_GR01_27897

## 1. Copiar los archivos necesarios al servidor
### (docker-compose.prod.yaml, .env.prod.template, init-db.sql)

## 2. Configurar el archivo de entorno
### Cambia de nombre al archivo 'env.prod.template' a '.env'

## 3. Ejecutar el despliegue
### docker-compose -f docker-compose.prod.yaml up -d

## 4. Crear BASE DE DATOS
docker cp init-db.sql acadance-postgres:/tmp/init-db.sql

docker exec acadance-postgres psql -U postgres -f /tmp/init-db.sql

LISTO Grupo 1
