# JUnit 4

1. Agregar JUni Test
2. Importar libreria
3. Notacion test

```java
@Test //JUnit lo reconoce como prueba unitaria
public void test(){}
```

4. Metodo fail hace que la prueba falle

```java
fail("asd");
```

5. Metodo de comparacion

```java
assertEquals(/*espectativa*/,/*Realidad*/);
```

6. Ejecutar metodos antes o despues de cad a prueba

```java
@Before
public void before(){}
```

```java
@After
public void after(){}
```

7. Metodos Assert

```java
assertEquals(/*Esperado*/,/*Obtenido*/)
```

```java
assertEquals(/*Esperado*/,/*Obtenido*/,/*MargenDeError*/)
```

```java
assertArrayEquals(/*Mensaje*/,/*Esperado*/,/*Obtenido*/)
```

```java
assertFalse(/*bool*/) //Si es falso
```

```java
assertTrue(/*bool*/)  //Si es verdad
```

```java
assertNotEquals(/*No Esperado*/,/*Obtenido*/)
```

```java
assertNotNull(/*valor*/)  //no es nulo
```

```java
assertNull(/*valor*/)   //es nulo
```

```java
assertSame(/*valor1*/,/*valor2*/)  //si se encuentran en el mismo epsaico de memoria
```

8. Parametros de la notacion Test

```java
@Test(expected=/*espera una excepcion que va a ocurrir*/.class)
```

```java
@Test(timeout=/*tiempo de espera*/)
```

9. Antes y despues depues de toda la clase

```java
@BeforeClass
public static void beforeClass(){}
```

```java
@AfterClass
public static void afterClass(){}
```

10. Pruebas parametrizada, crear un constructor

```java
@RunWith(value=Parameterized.class)
class ..{
    @Parameters //Contiene los datos
    public static Iterable<Object[]> getData(){
        List<Object[]> obj = new ArrayList<>();
        obj.add(new Object[]{3,4,7})
        obj.add(new Object[]{2,3,5})
        obj.add(new Object[]{3,3,6})
    }

    @Parameters //Contiene los datos
    public static Iterable<Object[]> getData(){
        return Arrays.asList(new Object[][]{
            {3,4,7},{2,3,5},{3,3,6}
        });
    }
}
```

11. Crear un suite para correr varias pruebas

```java
@RunWith(value=Suite.class)
@Suite.SuiteClasses({
    prueba1.class
    prueba2.class
})
```
