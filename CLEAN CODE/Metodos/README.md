# Métodos

### Reducidos
La primera norma de los métodos/funciones, es que deben ser de tamaño reducido.
Los métodos no deberían tener más de 20 líneas.

### Bloques e indentación
Los bloques que contengan un `if` , `else`, `while`... solamente deberían tener una línea. Probablemente esa línea sea una llamada a un método.

### Switch
Como norma general, los `switch` se permiten si aparece una única vez en el código, se utilizan para crear objetos [polimórficos](https://www.ecured.cu/Polimorfismo_(Inform%C3%A1tica) y se encuentran ocultos tras una relación de herencia de clases.

*Ejemplo:*
```java
public abstract class Employee {
	public abstract boolean isPayday();
	public abstract Money calculatePay();
	public abstract void deliverPay();
}

// --------------------------------------

public interface EmployeeFactory {
	public Employee makeEmployee(EmployeeRecord r) throws InvalidEmployeeType;
}

// --------------------------------------

public class EmployeeFactoryImpl implements EmployeeFactory {
	public Employee makeEmployee(EmployeeRecord r) throws InvalidEmployeeType {
		switch (r.type) {
			case COMMISSIONED:
				return new CommissionedEmployee(r);
			case HOURLY:
				return new HourlyEmployee(r);
			case SALARIED:
				return new SalariedEmployee(r);
			default:
				throw new InvalidEmployeeType(r.type);
		}
	}
}
```


### Nombes descriptivos
Un nombre largo y descriptivo es mejor que uno corto y confuso. Un nombre largo y descriptivo es mejor que un comentario largo y descriptivo.

### Argumentos
El número ideal de argumentos para un método es NINGUNO.

### Funciones monádicas (un argumento)
Si una función va a convertir el tipo de su argumento de entrada (por ejemplo un casteo), la conversión debe ser el *return type* de la función.

*Ejemplo:*
```java
// Función correcta
public StringBuffer transform(StringBuffer in)

// Función incorrecta
public void transform(StringBuffer out)
```

### Flags
Un *flag argument* es un parámetro que condiciona la funcionalidad del método.
Es decir, el método hace una cosa u otra en función del argumento.
Es recomendable evitar este tipo de parámetros. Pasar un boleano a un método, por lo general es una mala práctica.

### Argument Objects
Cuando una función necesita más de dos o tres argumentos, por lo general varios de estos argumentos pueden ser agrupados en una clase (*wrapped*) propia.

*Ejemplo:*
```java
// Incorrecto
public Circle makeCircle(double x, double y, double radious);

// Correcto
public Circle makeCircle(Point center, double radious);
```

### Listas de argumentos
Podemos hacer uso de *variadic params* en funciones repetitivas de **N** argumentos.

*Ejemplo:*
```java
public String format(String format, Object... args);
```

### Evitar los efectos colaterales
Si la función va a producir *side effects*, se debe expresar claramente en el nombre de la función, y por lo general su *return type* será `void`.

### Command Query Separation
Los métodos deben modificar/hacer algo, o responder a algo, pero no ambas cosas.

### Mejor excepciones que devolver errores
Devolver códigos de erro en las funciones en lugar de elevar excepciones es una violación del *Command query separation principle*.

### Extraer bloques de los Try/Catch
Es mejor extraer el código de los bloques  `try` y `catch` a funciones.

### El manejo de errores es una responsabilidad
Las funciones deben tener una única responsabilidad, y el manejo de errores es una responsabilidad.
Si existe un `try` en una función, debe ser la primera palabra de esta, y la función debe acabar tras el bloque de `catch/finally`.


> **Robert C. Martin:** *En ocasiones, empeorar el tiempo de procesamiento de un método reduciendo su eficiencia puede ser beneficioso en cuanto a facilitar la compresión del código y reducir el tiempo y esfuerzo invertido por otro programador en entenderlo.*