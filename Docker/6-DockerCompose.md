# Docker Compose

Describe la arquitectuar de servicio en un archivo

```
instalar docker compose
```

> yml

```
version: "3.8" //features soporta con los servicios

services: //servicios que utilizan la aplicacion
    app:
        image: /**/
        enviroment: // variables de entorno
            MONGO_URL: "mongodb://db:2017"
        depends_on: // contenedor dependiente
            - db
        ports:
            - "3000: 3000"

    db:
        image: mongo
```

> un servicio puede tener uno o mas contenedores de una misma imagen

1. Ejecutar

```
docker-compose up
```

2. Corre en el back

```
docker-compose up -d
```

3. visualizar contenedores

```
docker-compose ps
```

4. Correr comando

```
docker-compose exec /*app*/ bash
```

5. limpiar entorno

```
docker-compose down
```

## docker como herramienta

```
version: "3.8" //features soporta con los servicios

services: //servicios que utilizan la aplicacion
    app:
        build: .  //ruta
        enviroment: // variables de entorno
            MONGO_URL: "mongodb://db:2017"
        depends_on: // contenedor dependiente
            - db
        ports:
            - "3000: 3000"

    db:
        image: mongo
```

Ejecutar

```
docker-compose build
```

Buildear servicio

```
docker-compose build /*servicio*/
```

Ejecutar cambio

```
docker-compose up-d
```

Vincular archivos

```
version: "3.8" //features soporta con los servicios

services: //servicios que utilizan la aplicacion
    app:
        build: .  //ruta
        enviroment: // variables de entorno
            MONGO_URL: "mongodb://db:2017"
        depends_on: // contenedor dependiente
            - db
        ports:
            - "3000: 3000"
        volumes:        //bind mount
            - .:/usr/src  //directorios vinvculados
            - /usr/src/node_modules //conservar
        command: npx nodemon index.js

    db:
        image: mongo
```

## Override

Colaboracion
