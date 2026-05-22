# Documentacion de contenedores de sistemas gestores de bases de datos

![Imagen Docker](./img/imagen_docker.png)

## Contenedor de Tutorial de Docker 

docker pull docker/getting-started

docker run -d -p 80:80 docker/getting-started

- -d deach (El proceso del contenedor se ejecuta en background)

- -p (port, publish) (Mapea el puerto)

- -docker /getting-started (Nombre de la Imagen)

## Contenedor del DBMS MariaDB
docker pull mariadb:lts-ubi9


## Comandos Docker 
| Comando | Descripcion 
| docker pull nombre_imagen | **Descarga una imagen docker** [Docker Hub](https://hub.docker.com/) 
| docker images   | **Visualizar las imagenes que se encuentran en el docker**  
| Fila 2    | Dato B    |