**Ron Jeffries:** *One method must says clearly what id does, and its submethos must say how it is done.*


### Usa nombres que revelen la intención
El nombre de una variable, método, o clase, debe contestar todas las grandes preguntas. Debe decir por qué existe, qué hace, y como se utiliza.


### Evita la desinformación
No te refieras un grupo de *accounts* como `accountList` a menos que sea un objeto de tipo `List`.
La palabra `List` tiene un significado específico para los programadores. Si el objeto que contiene las *accounts* no es un objeto de tipo `List`, esto puede dar lugar a confusión.
Otros nombres de variable como `accountGroup`, `bunchOfAccounts` o simplemente `accounts` pueden ser una mejor elección.
Cuidado con usar nombres de variables parecidos.


### Utiliza nombres fáciles de buscar
Por ejemplo, en una clase con mucho volumen de código, sería más fácil encontrar la constante `WORK_DAYS_PER_WEEK` que encontrar el número `5`.


### Interfaces e implementaciones
Deja limpio el nombre de la interfaz, y para distinguirla de su implementación, modifica el nombre de la implementación.

*Ejemplo:*
```java
// Mala nomenclatura
IEmployeeFactory // Interfaz
EmployeeFactory  // Implementación

// Buena nomenclatura
EmployeeFactory     // Interfaz
EmployeeFactoryImpl // Implementación
```


### Nombres de clases
El nombre de una clase no debería ser un verbo.