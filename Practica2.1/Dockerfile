#partiendo de una imagen con php
FROM php:7.4-cli
#copia aplicacion php al directorio /tmp del contenedor
COPY ./aplicacion.php /tmp 
#establecer directorio /tmp como directorio de trabajo
WORKDIR /tmp
#ejecutamos la aplicacion
CMD [ "php", "./aplicacion.php" ]
