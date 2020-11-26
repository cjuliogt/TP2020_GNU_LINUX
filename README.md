#  Trabajo Practico 

Materia: Administracion  de Sistemas GNU/LINUX  y Virtualizacion Avanzada

## ● Creación de un ambiente Cloud utilizando owncloud
-------------------------------------------------------

### Crear un directorio 

mkdir owncloud-docker-server

### Cambiar de directorio

cd owncloud-docker-server

### Clonar un repositorio 

wget https://raw.githubusercontent.com/owncloud/docs/master/modules/admin_manual/examples/installation/docker/docker-compose.yml

### Crear un archivo de configuracion de entorno 

cat << EOF > .env 

OWNCLOUD_VERSION=10.5

OWNCLOUD_DOMAIN=localhost

ADMIN_USERNAME=admin

ADMIN_PASSWORD=admin

HTTP_PORT=8080

EOF

### Habilitar e iniciar el contenedor 

sudo docker-compose  up -d 


## Comando útiles para el servicio de Owncloud

### Ayuda en el servicio de ownCloud 
sudo  docker-compose exec owncloud occ -h

### Mostrar lista de comandos en ownCloud 
sudo  docker-compose exec owncloud occ list 

### Agregar un usuario 
sudo  docker-compose exec owncloud occ user:add  --display-name=“nombre_usuario”  --email=ejemplo@ejemplo.com –group=“users” nombre_usuario – 

### Instalar aplicaciones
sudo  docker-compose exec owncloud occ market:install extract ( Plugin permite descargar archivos de la nube) 

###  Visualizar las aplicaciones disponibles en la tienda 
sudo  docker-compose exec owncloud occ market:list


## Bibliografía 

https://doc.owncloud.com/server/10.5/admin_manual/ownCloud_Admin_Manual.pdf



