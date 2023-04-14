# Configuración de una DB postgres con docker-compose

## Instalación

Descargar las fuentes con
```
git clone https://github.com/foxmoyano/docker.git
```
## Configuración

Se debe entrar a la carpeta **docker/postgres.**

Hay que generar un archivo .env para indicar las valores a usar como el nombre del contenedor, el puerto y las credenciales de la base  de datos.

.env
```
PROJECT_NAME=

POSTGRES_USER=
POSTGRES_PASS=
POSTGRES_DB=
POSTGRES_PORT=
```

## Ejecución

```
docker-compose up -d
```
