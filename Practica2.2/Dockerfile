#partimos de una imagen de ubuntu
FROM ubuntu:latest
#seleccionamos el directorio del contenedor
WORKDIR /home
#actualizar listas de dependencias
RUN apt-get update -y
#configuramos tzdata como "no interactivo" para que no solicite el área geográfica al instalar php
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y tzdata
#instalamos apache y git (necesario para ejecutar posteriormente git clone)
RUN apt-get install -y apache2 git
#exponemos el puerto 80
EXPOSE 80
#nos movemos al directorio de apache
WORKDIR /var/www/html
#descargamos la aplicación php de un repositorio de git
RUN git clone https://github.com/drnic/php-helloworld.git
#instalamos php
RUN apt-get install -y php
#arrancamos el servicio apache en segundo plano
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
