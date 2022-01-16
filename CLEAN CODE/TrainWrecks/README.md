# TRAIN WRECKS
**No se debe anidar métodos en cadena.**
**En el caso de anidar métodos de objetos en POO, esta práctica violaría la *Ley de Demeter*.**
**Pide las acciones, y no información para hacerlas.**

*Ejemplo:*

```java
// Para comprobar si un usuario es mayor de edad
// ***** Ejemplo de mal código *****
usuario.getEdad().getValue() > 18

// ***** Ejemplo de como hacerlo *****
usuario.isLegalAge()
```
