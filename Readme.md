# Taller Introducción a Docker
Este repositorio incluye toda la información mostrada en el taller. En él se encuentra la presentación mostrada y todos los proyectos usados en la demo.

## Presentación

[Presentación](Presentacion-Docker.pdf)

## Enlaces de interés
A continuación se muestran los enlaces de interés mostrados en la presentación:

 - [Instrucciones para la creación de un Dockerfile](https://docs.docker.com/engine/reference/builder/)
 - [Comandos CLI](https://docs.docker.com/engine/reference/commandline/docker/)
 - [Comando Build](https://docs.docker.com/engine/reference/commandline/build/)
 - [Comando Run](https://docs.docker.com/engine/reference/commandline/run/)

## Ejemplos
A continuación se muestran los comandos usados para cada ejemplo:

### Construcción Dockerfile básico
Este ejemplo tiene como objetivo entender el funcionamiento de los Dockerfiles y la construcción de imágenes.

Los comandos usados son:

1. Construcción de la imagen
```sh
docker build -t demo --build-arg arg1="Hola Mundo desde ARG" .
```

2. Creación del contenedor
```sh
docker run -d --name demo demo
```

3. Ejecución de comandos dentro del contenedor
```sh
docker exec -it demo bash
```


### NGINX
Este ejemplo muestra como crear un servidor de recursos estáticos dentro de un contenedor.

Los comandos usados son:

1. Construcción de la imagen
```sh
docker build -t nginx:basic .
```

2. Creación del contenedor
```sh
docker run --name nginx:basic -d -p 8080:80 nb1
```

3. Ejecución de comandos dentro del contenedor
```sh
docker exec -it nb1 bash
```

### NGINX con persistencia
Este ejemplo muestra como crear un servidor de recursos estáticos dentro de un contenedor con persistencia.

Los comandos usados son:

1. Construcción de la imagen
```sh
docker build -t nginx:vol .
```

2. Creación del contenedor
```sh
docker run --name nginx:vol -d -p 8080:80 nv1
```

3. Ejecución de comandos dentro del contenedor
```sh
docker exec -it nv1 bash
```

### Spring
Este ejemplo muestra como desplegar una aplicación de Spring con Docker.

Los comandos usados son:

1. Construcción de la imagen
```sh
docker build -t hero --build-arg JAR_FILE=${PATH_DEL_JAR} .
```

2. Creación del contenedor
```sh
docker run -p 8080:8080 hero
```