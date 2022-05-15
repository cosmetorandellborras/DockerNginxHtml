# DockerNginxHtml

## Objetivos

Los objetivos de esta práctica son realizar la instalación de Nginx en Docker y posteriormente desplegar una web en nuestro servidor Nginx dockerizado.

## Paso 1 - Instalación del contenedor Nginx

Para realizar la instalación del contenedor Nginx en Docker en primer lugar nos dirigimos a la web "Docker Hub", buscaremos el contenedor Nginx oficial y seguidamente copiaremos el comando "pull" indicado.

![dockerhub](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/dockerhub.png)

Segidamente, ejecutamos el comando en nuestra terminal, esto hara que se descargue e instale una imagen del contenedor Nginx
~~~
docker pull nginx
~~~
![dockerpull](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/docker%20pull.png)

## Paso 2 - Verificar la instalación del contenedor Nginx

Para verificar la instalación ejecutaremos el siguiente comando, que arrancara nuestro contenedor con Nginx.
~~~
docker run --rm -d -p 8080:80 --name web nginx
~~~
![dockerRun](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/docker%20run.png)
Seguidamente, abrimos nuestro navegador e insertamos siguiente dirección.
~~~
localhost:8080
~~~
Si todo ha ido bien tenemos que visualizar el mensaje de bienvenida de Nginx
![landingNginx](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/landingNginx.png)

Antes de pasar al paso 3, pararemos el microservicio Nginx con el siguiente comando

~~~
docker stop web
~~~

## Paso 3 - Creación del directorio y html

En este paso crearemos un directorio que almacenará nuestro html.
Para ello creamos un directorio en nuestra carpeta de Documentos que llamaremos nginx, y dentro de este una carpeta que llamaremos "www".

![Directorio](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/Directorio.png)

Seguidamente crearemos un archivo html dentro del directorio "www" creado en el paso anterior.
![nano1](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/nano.png)
![nano2](https://github.com/cosmetorandellborras/DockerNginxHtml/blob/main/nano2.png)

## Paso 4 - Iniciar contenedor Nginx con html personalizado


