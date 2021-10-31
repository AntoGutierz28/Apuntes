# Datos en docker

1. Contenedor de mongo

```
docker run -d --name db mongo
```

2. Activar la consola

```
docker exec -it db bash
```

## Bind mount

- Directorio que se quiere montar en el contenedor

1. Contenedor de mongo y enlazar a un directorio local

```
docker run -d --name db -v /*ruta completa*/:/*ruta del contenedor*/ /*tipo de container*/
```

> Seguridad en enlazar directorios con datos sensibles

## Volumenes

- Mas seguridad que los bind Mount, espacio de disco manejado por docker

1. Visualizar volumenes

```
docker volume ls
```

2. Crear volumen

```
docker volume create /*name*/
```

3. correr containes con docker

```
docker run -d --name /*name*/ --mount src=/*nombre de volumen*/,dst=/*ruta*/ /*tipo de container*/
```

## Ingresar o extraer archivos

1. Copiar archivo al contenedor

```
docker cp /*archivo*/ /*name*/:/*ruta/nombre*/
```

2. Extraer archivo

```
docker cp /*name*/:/*ruta*/ /*directorio a extraer*/
```

> Se puede extraer archivo sin importar estado del contenedor

> tmpfs porcion de disco que solo tiene en memoria del contenedor, temporales (solo en linux)
