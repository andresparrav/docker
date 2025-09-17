# Commands Docker

<p align="center">
  <img src="https://github.com/andresparrav/docker/blob/main/docker1.png" width="800"/>
</p>


## Comandos basicos

¿Cómo verificar la versión de Docker instalada?
Una acción básica para comprobar nuestra instalación es utilizar la línea de comandos con el comando:
```
docker version
```

¿Qué información relevante aporta docker info?
Puedes acceder a detalles importantes sobre el hardware disponible o asignado a Docker en tu sistema. Muestra especificaciones relevantes como la memoria, procesador y GPU disponibles, información útil para decidir futuros ajustes en tu equipo.
```
docker info
```

¿Cuáles son los comandos básicos equivalentes a Docker Desktop?
Docker Desktop tiene una interfaz visual amigable, pero es fundamental conocer su equivalente en línea de comandos. Estos son algunos ejemplos clave que puedes memorizar:

* Listar imágenes disponibles:
```
docker images
```
* Ver contenedores activos:
```
docker ps
```
* Explorar opciones de comandos específicos con ayuda:
```
docker images --help
```
Crear imágenes a partir de archivos Dockerfile.
```
docker build
```
Ejecutar contenedores a partir de imágenes disponibles.
```
docker run
```
Ambos comandos tienen múltiples parámetros, pero la documentación proporcionada al utilizar --help facilita enormemente entender cada opción y explicación disponible.
```
docker build --help
docker run --help
```


## Comandos para imagenes:

| Description      | Syntax |
| ----------- | ----------- |
| Construir una imagen a partir de un archivo Dockerfile: | docker build -t <nombre_de_imagen> |
| Construir una imagen desde un archivo Dockerfile sin la caché | docker build -t <nombre_de_imagen> . -no-cache |
| Listar imágenes locales | docker images |
| Eliminar una imagen | docker rmi <nombre_imagen> |
| Eliminar todas las imágenes no utilizadas |  docker image prune |
| Levanta todos los servicios definidos en un archivo docker-compose.yml. Por ejemplo: | docker-compose up |
| docker-compose down: Detiene y elimina todos los contenedores definidos en un archivo docker-compose.yml. Por ejemplo: | docker-compose down |


## Comandos para contenedores

| Description      | Syntax |
| ----------- | ----------- |
| Crea y ejecuta un contenedor a partir de una imagen, con un nombre personalizado: | docker run --name <nombre_contenedor> <nombre_imagen> |
| Ejecutar un contenedor con y publicar un puerto(s) del contenedor al host. | docker run -p <puerto_host>:<puerto_contenedor> <nombre_imagen> |
| Ejecutar un contenedor en segundo plano | docker run -d <nombre_imagen> |
| Iniciar o detener un contenedor existente: | docker start|stop <nombre_del_contenedor> (o <id_del_contenedor>) |
| Eliminar un contenedor detenido: | docker rm <nombre_del_contenedor> |
| Abrir un shell dentro de un contenedor en ejecución: | docker exec -it <nombre_del_contenedor> sh |
| Obtener y seguir los logs de un contenedor: | docker logs -f <nombre_contenedor> |
| Inspeccionar un contenedor en ejecución: | docker inspect <nombre_del_contenedor> (o <id_del_contenedor>) |
| Para listar los contenedores actualmente en ejecución: | docker ps |
| Listar todos los contenedores docker (en ejecución y parados): | docker ps --all |
| Ver las estadísticas de uso de recursos | docker container stats |


Referencia: https://docs.docker.com/get-started/docker_cheatsheet.pdf
