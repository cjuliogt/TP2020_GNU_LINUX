#  Trabajo Practico 

Materia: Administracion  de Sistemas GNU/LINUX  y Virtualizacion Avanzada

## ● Creación de un ambiente Cloud utilizando owncloud
-------------------------------------------------------

### Crear un directorio 

mkdir owncloud-docker-server

### Cambiar de directorio

cd owncloud-docker-server

### Clonar un repositorio 

git clone https://github.com/cjuliogt/TP2020_GNU_LINUX.git

### Crear un archivo de configuracion de entorno 

cat <<EOF> .env
OWNCLOUD_VERSION=10.5
OWNCLOUD_DOMAIN=localhost,"192.165.0.105"
ADMIN_USERNAME=admin
ADMIN_PASSWORD=admin
HTTP_PORT=8080

### Habilitar e iniciar el contenedor 

sudo docker-compose  up -d 


