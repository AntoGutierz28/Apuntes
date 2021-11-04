# Docker en el desarrollo

> "." --> Donde estoy ubicado

1.  Copiar un archivo

```
COPY ["Ubicacion emisor", "Ubicacion receptor"]
```

2. Directorio de trabajo

```
WORKDIR /*UBICACION RECEPTOR*/
```

3. Instalar

```
RUN npm install
```

4. Puerto a utilizar

```
EXPOSE 3000
```

5. Comando a correr

```
CMD ["node","index.js"]

CMD node index.js
```

6. Ejecutar imagen

```
docker build -t /*nombre*/ /*direccion*/
```

7. Imagenes

```
docker image ls
```

> --rm eliminar el contenedor cuando se deje de usar

```
docker run --rm -p 3000:3000 /*contenedor*/
```

## layer cache

- Utilizar capa ya existentes
- Si se cambia una linea de dato se tiene que hacer build nuevamente
- Se puede reutilizar siempre y cuando no se haya modificado alguna dependencia

> -v

## docker networking

Conectar contenedores

1. Muestra las redes por defecto de docker

```
docker networking ls
```

2. crear network

```
docker network create --attachable /*nombre*/
```

3. conectar contenedor a la red

```
docker network connect /*nombre red*/ /*nombre contenedor*/
```

> --env

4. enlazar contenedores

```
docker run -d --name app -p 3000:300 --env /*variable*/=/*ruta con el nombre del contenedor*/
```
