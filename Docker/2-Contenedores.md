# Contenedores

- Correr un contenedor. Crea un contenedor y lo ejecuta.

```
docker run /*hello-world*/
```

## Que es un contenedor

> "Una maquina virtual liviana"

Agrupacion de procesos que corre nativamente en el sistema pero esta encapsulada, se puede limitar los recursos de la computadora. Solo corre un proceso del Sistemas operativo

- Mostrar los contenedores corriendo

```
docker ps
```

- Mostrar todos los contenedores

```
docker ps -a
```

- Informacion de los contenedores

```
docker inspect /*ID-Container*/
```

> Name en docker es como un alias del contenedor, generado por docker automaticamente y es unico por container

- Otorgar nombre al contenedor

```
docker run --name /*nombre*/ /*contenedor*/
```

- Cambiar nombre del contenedor

```
docker rename /*nombre actual*/ /*nombre nuevo*/
```

- Eliminar contenedores

```
docker rm /*ID o name*/
```

- Eliminar todos contenedores terminados

```
docker container prune
```

## Correr un Ubuntu entero

- Correr un ubuntu entero

```
docker run ubuntu
```

> Comand es el proceso que corre al arrancar

- Correr un ubuntu modo interactivo

```
docker run -it ubuntu
```

> cat /etc/lsb-release

# Ciclo de vida de un contenedor

1. El contenedor se detiene cuando terminamos su proceso principal
2. Se mantiene activo el container

```
docker run --name /*name*/ -d ubuntu tail -f  /dev/null
```

3. Ejecutar un proceso en un contenedor existente y corriendo

```
docker exec -it /*name*/ bash
```

> ps -aux //procesos

4. Conocer el proceso principal del contenedor

```
docker inspet --format '{{.State.Pid}}' /*name*/
```

5. Terminar el proceso principal solo con Linux

```
kill -9 /**/
```

> nginx proxy reverso

6. Crear proxy nginx

```
docker run -d --name proxy nginx
```

> Cada contenedor posee su propia iterfaz de red

7. Apagar un contenedor

```
docker stop /*name*/        //Para el contenedor
docker rm -f /*name*/       //Para y elimina
```

> -d para que el contenedor corra de background 8. Asignar puerto de local

```
docker run -d --name proxy -p /*puerto anfitrion*/:/*puerto contenedor*/ nginx
```

9. Visualizar el log del contenedor

```
docker logs /*name*/         //view log
docker logs -f /*name*/      //ver log time real
docker logs --tail /*cantidad*/ -f /*name*/ //ultimos logs
```
