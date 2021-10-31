# Docker

Construir, distribuir y ejecutar aplicaciones, corre en Linux

## Problemas que trata de resolver

- Enterno de desarrollo
- Dependencias
- Entorno de ejecucion
- Equivalencia con entorno productivo
- Servicio exteros(Base de datos)

## Virtualizacion

Version virtual de ercursos tecnologicos.

- Peso en GB's
- Costo sw administracion
- Multiples formatos

## Preparar entorno de trabajo

- Docker desktop
- Docker Hub = Repositorio de docker
- Play with Docker = Cloud, tiempo limite de 4 horas

## Version de docker

```
docker --version
```

## Info de instalacion

```
docker info
```

## Play with docker

Iniciar sesion con cuenta de Docker Hub
https://labs.play-with-docker.com/

- Sesion en la nube
- Dura 4 horas

### Pasos a seguir

1. Crear instancia
2. Utilizar todo el la base de linux
3. Se mantiene el link enlazada con la instancia.

## Definicion

- Plataforma que permite construit, ejecutar y compartir aplicaciones

1. Docker daemon: server de docker, maneja las entidades que nos permite urilizar los contenedores
2. REST API: expone una interfaz para comunicarse
3. Docker CLI: cliente de Docker, manda las instrucciones al Docker daemon
4. Contenedores: corazon de Docker
5. Image: artfactos de docker para empaquetar conetndores o codigos
6. Data volumes: permite acceder al sistema de archivos al sistema anfitrion
7. Network: Comunicar vomponentes de Docker
