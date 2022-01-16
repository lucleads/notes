# Concurrencia
La [concurrencia](./../Conceptos) es una estrategia de desacoplamiento. Ayuda a separar **que se hace** de **cuando se hace**.

### Mitos de la concurrencia

> *Siempre mejora el rendimiento*

La concurrencia puede mejorar el rendimiento, pero solo cuando existe un gran tiempo de espera que puede ser distribuido en distintos hilos o procesadores.

> *El diseño no cambia al escribir programas concurrentes*

La concurrencia suele implicar un gran cambio sobre la estructura del sistema.

> *Entender los problemas de concurrencia no es importante cuando trabajamos en entornos como Web o [EJB](https://www.javatpoint.com/what-is-ejb)*

Los problemas de concurrencia pueden aparecer en cualquier entorno.


### Principios de la concurrencia

**Principio de Responsabilidad Única (SRP)**

Manten el código dirigido a manejar problemas de concurrencia separado del resto del código.
***
**Limitar la accesibilidad de la información**

Modificar algún campo en un objeto compartido puede interferir con otro, causando un error inesperado. Una solución es usar la keyword `synchronized` para proteger la *sección crítica* en el código que usa el objeto compartido.

Hay que tomarse en serio la encapsulación de la información, teniendo muy en cuenta el acceso a cualquier información que pueda ser compartida.
***
**Usar copias de la información**

En algunas ocasiones es posible crear copias de objetos y utilizar estos como `read-only`. En otras, es posible copiar objetos, recolectar la información de diferentes hilos en estas copias, y una vez recolectada toda la información, hacer el merge de esta en un único hilo.
***
**Los hilos deben ser tan independientes entre ellos como sea posible**
Debemos intentar separar la información en subconjuntos independientes que puedan ser operados en diferentes hilos, que probablemente puedan ejecutarse en diferentes procesadores.
***

**Recomendaciones:**
- Aprende los algoritmos básicos del lenguaje que utilices, y comprende las soluciones propuestas
- Evita usar más de un método en un objeto compartido
- Mantén tus `synchronized sections` tan pequeñas como sea posibles
- Escribe tests que puedan exponer los problemas y ejecutarlos de forma frecuente, con diferentes configuraciones programadas y configuraciones del sistema y carga
- No ignores los fallos del sistema que creas que son algo puntual
- Asegurate de que tu código funciona de forma independiente a los hilos que lo ejecutan
