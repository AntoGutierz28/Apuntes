# Maven

## Creacion de proyecto con maven

    		La estructura del proyecto   nombre del proyecto

mvn archetype:generate -DgroupId=com.mycompany.app -DartifacId=simple-app
todo por defecto
mvn archetype:generate -DgroupId=com.mycompany.app -DartifacId=simple-app -DinteractiveMode=false

Consola

```
mvn archetype:generate -DgroupId=com.mycompany.app -DartifacId=simple-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

Web

```
mvn archetype:generate -DgroupId=com.mycompany.app -DartifacId=simple-app -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false
```

## Compilar el proyecto

/target

```
mvn compile
```

## Ejecutable

jar

```
mvn package
```

## Limpiar

limpia /target

```
mvn clean
```

# Project Object Model (POM)

-Contiene como funcion
-Repositorio: https://mvnrepository.com/

## Agregar dependencia en

```xml
<dependencies></dependencies>
```

## Establecer el JDK a utilizar

```xml
<properties>
<maven.compiler.source>1.8</maven.compiler.source>
<maven.compiler.target>1.8</maven.compiler.target>
</properties>
```

## Actualizar proyecto

Eclipse => Anticlick en el proyecto->maven->update project

### Limpiar archivos creados por eclipse

```
mvn eclipse:clean
```

## Generar los archivos para el reconocimieto por eclipse

```
mvn eclipse:eclipse
```

## Las clases los guarda poara ser utilizada en otros proyectos

mvn install

## Ejecutar el profile

```
mvn -P qa package
```

## POM multiple

```
mvn -f POM.xml package
```

## Dependencias transitivas

### Dependencias indirectas

---

## Excluir dependencia

```xml
<exclusions> groupId - artifacID</exclusions>
```

---

## Documentacion de la app

```
mvn site
```

```xml
<build>
<plugins>
<groupId>org.apache.maven.plugins<groupId>
<artifactId>maven-site-plugin<artifactId>
<version>3.7.1</version>
<configuration><!--Idiomas-->
<locales>enfr</locales>
</configuration>
</plugins>
</build>

<reporting>
<plugins>
<groupId>org.apache.maven.plugins<groupId>
<artifactId>maven-javadoc-plugin<artifactId>
<version>3.0.1</version>
<configuration><!--Idiomas-->
<locales>enfr</locales>
</configuration>
</plugins>
</reporting>
```
