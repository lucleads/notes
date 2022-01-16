# LA LEY DE DEMETER

***Un objeto/módulo solamente debe necesitar conocer sus componentes, y no componentes externos o subcomponentes***

Un método ***f*** de la clase **C** solo puede llamar a métodos de:
- **C**
- Un objeto creado por ***f***
- Un objeto pasado como argumento a ***f***
- Un objecto contenido en una variable de **C**

El método no debe invocar métodos de objetos devueltos por las funciones permitidas.

*Ejemplo:*
```java
// Viola la ley de Demeter
String oddStreetNumbers = users
    .getAddress()
	.stream()
    .filter(address::numberIsOdd)
    .getStreet()
    .collect(Collectors::toList)

// Forma correcta
String userStreet = users
    .stream()
	.filter(user::getOddStreets)
	.collect(Collectors::toList);
```

![[./../imagenes/law-of-demeter.png]]
