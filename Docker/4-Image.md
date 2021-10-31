# Imagenes

Plantillas o moldes de donde docker crea contenedores
Analigia
Imagenes --> Clase
Contenedor --> Objeto

- Visualizar Imagenes

```
docker image ls
```

> TAG versiond e la imagen

- Extraer una imagen

```
docker pull /*imagen*/:/*version*/
```

## Crear imagen

Parte de docker file

1. Crear Dockerfile

```docker
FROM ubuntu:latest               //Todo imagen parte de algo mas

RUN touch /usr/src/anker.txt    //Comando que va a correr, se ejecuta en tiempo de build
```

2. Ejecutar imagen

```
docker build -t ubuntu:/*tag*/ /*ruta ". para directorio actual" */
```

Resulatdo 2 ID, de las capas.

> Imagen es un conjunto de capas

3. docker logincon la cuenta de docker hub

4. Cambiar de nombre al contenedor

```
docker tag ubuntu:/*tag*/ /*nuevo nombre*\/ubuntu:/*tag*/
```

5. Publicar imagen

```
docker push /**nombre de usuario de doxker hub*\/ubuntu:/*tag*/
```
