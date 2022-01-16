# LAS NORMAS DE KENT BECK'S RULES
>**Kent Beck establece cuatro normas básicas para un buen diseño de software. Las normas son las siguientes en orden de prioridad:**

### 1. Ejecuta todos los tests
Un sistema que está adecuadamente testeado y pasa siempre todos sus tests es un sistema testable. Los sistemas no testables no son tampoco fiables.

### 2. No contiene duplicidad
La duplicidad es el mayor enemigo de un sistem con un buen diseño. Representa trabajo adicional, riesgo adicional y complejidad innecesaria adicional.

### 3. Expresa la intención del programador
Es necesario elegir buenos nombres, y mantener las clases y funciones con un tamañor reducido.
Debemos utilizar nomenclaturas estandar. Los patrones de diseño por ejemplo, suelen ir orientados a facilitar la comunicación y expresividad. Utilizar nombres de patrones como *COMMAND* o *VISITOR* en los nombres de nuestras clases facilita describir su funcionalidad a otros programadores.
Los tests también deben ser expresivos e indicar su función.

### 4. Minimizar el número de clases y métodos
No debemos crear clases que no acomenten una función. Por ejemplo la práctica de definir siempre una interfaz para cada clase, resulta en una estructura de clases enorme en innecesaria, por lo que debemos pararnos a pensar si una clase es realmente necesaria antes de introducirla en nuestro programa.