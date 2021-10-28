# Mockito

## Mocks

Es un objeto que simula ser otro para suplantarloen un entorno determinado. Simula dependencias internas o externas

1. Utilizar mockito

```java
@RunWith(MockitoJUnitRunner.class)
```

2. Declarar instancia

```java
@InjectMocks    //Dependiente
Calculadora calc = new Calculadora();
```

3. Se declara la dependencia

```java
@Mock           //Dependencia
CalculadoraOracle calcOc;
```

4. Crear "escenarios"

```java
@Before
public void before(){
    when(var.sumar(5,5)).thenReturm(10.0);
    when(var.sumar(5,5)).thenReturm(10.0);
}
```
