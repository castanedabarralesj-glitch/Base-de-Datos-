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

## Contenedor de MariaDB sin volumen 
docker run --name ServerMariaDBG2 -e MARIADB_ROOT_PASSWORD=123456 \
-d -p 3345:3306  e0236 

## Comandos Docker 
| Comando | Descripcion |
| docker pull nombre_imagen | **Descarga una imagen docker** [Docker Hub](https://hub.docker.com/) |
| docker images   | **Visualizar las imagenes que se encuentran en el docker**  |
| Fila 2    | Dato B    |
| docker ps   | **Visualizar los contenedores que estan encendidos**  |
| docker ps -a  | **Visualizar todos los contenedores que estan encendidos y apagados**  |
|docker stop idcontenedor o nombredelcontenedor | **Detiene un contenedor**  |
|docker start idcontenedor o nombredelcontenedor | **Enciende un contenedor**  |
|docker rm | **Elimina un contenedor si esta apagado**  |
|docker rm -f id contenedor o nombrecontenedor | **Elimina un contenedor este o no encendido**  |


## Contenedor de mariaDB con volumen ##
docker run --name ServerMariaDBG2 -e MARIADB_ROOT_PASSWORD=123456 \
-d -v V-MariaDBG2:/var/lib/mysql -p 3345:3306  e0236 

## Contenedor de postgres con volumen ##
docker run --name ServerPostgresG2 -e POSTGRES_PASSWORD=123456 \
-d -p 5457:5432 -v V-PostgresG2:/var/lib/postgresql/data \ 
eba8d

## contenedor sql server ##
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=P@ssw0rd" \
   -u 0 \
   -p 1452:1433 --name SQLServerG2\
   -d -v V-sqlServerG2:/var/opt/mssql/data \
   sha25 
