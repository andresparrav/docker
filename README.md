# Commands Docker

## Comandos para imagenes:

| Syntax      | Description |
| ----------- | ----------- |
| docker build -t <nombre_de_imagen> | Construir una imagen a partir de un archivo Dockerfile: |
| docker build -t <nombre_de_imagen> . -no-cache | Construir una imagen desde un archivo Dockerfile sin la caché |
| docker images | Listar imágenes locales |
| docker rmi <nombre_imagen> | Eliminar una imagen |
| docker image prune | Eliminar todas las imágenes no utilizadas | 


## Comandos para contenedores

| Syntax      | Description |
| ----------- | ----------- |
| docker run --name <nombre_contenedor> <nombre_imagen> | Crea y ejecuta un contenedor a partir de una imagen, con un nombre personalizado: |
| docker run -p <puerto_host>:<puerto_contenedor> <nombre_imagen> | Ejecutar un contenedor con y publicar un puerto(s) del contenedor al host. |
| docker run -d <nombre_imagen> | Ejecutar un contenedor en segundo plano |
| docker start|stop <nombre_del_contenedor> (o <id_del_contenedor>) | Iniciar o detener un contenedor existente: |
| docker rm <nombre_del_contenedor> | Eliminar un contenedor detenido: |
| docker exec -it <nombre_del_contenedor> sh | Abrir un shell dentro de un contenedor en ejecución: |
| docker logs -f <nombre_contenedor> | Obtener y seguir los logs de un contenedor: |
| docker inspect <nombre_del_contenedor> (o <id_del_contenedor>) | Inspeccionar un contenedor en ejecución: |
| docker ps | Para listar los contenedores actualmente en ejecución: |
| docker ps --all | Listar todos los contenedores docker (en ejecución y parados): |
| docker container stats | Ver las estadísticas de uso de recursos |


Referencia: https://docs.docker.com/get-started/docker_cheatsheet.pdf
