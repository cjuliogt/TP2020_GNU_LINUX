##Trabajo Practic o - Administracion GNU/LINUX  

Instalacion de onwCloud a partir de Docker-compose

-------------------------------------------------------
Crear un directorio 

mkdir owncloud-docker-server

Cambiar de directorio 

cd owncloud-docker-server

Clonar el repositorio 

git clone https://github.com/cjuliogt/TP2020_GNU_LINUX.git

Crear el archivo de configuracion de entorno 

cat <<EOF> .env
OWNCLOUD_VERSION=10.5
OWNCLOUD_DOMAIN=localhost,"192.165.0.105"
ADMIN_USERNAME=admin
ADMIN_PASSWORD=admin
HTTP_PORT=8080

H            abilitar e inic iar el contenedor 

sudo docker-compose  up -d 


