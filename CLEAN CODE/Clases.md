# Clases

### Encapsulación
Aunque debemos mantener la encapsulación de nuestras clases, funciones y variables manteniéndolas privadas, los tests mandan, por lo que si un test necesita llamar a una función o acceder a una variable, deberemos modificar su visibilidad.
Aún así, trataremos de mantener su privacidad, y perder la encapsulación será siempre el último recurso a utilizar.

### Mantener la cohesión
Si en una clase tenemos funciones que comparten variables, probablemente estas funciones constituyan en realidad una nueva clase.
Cuando las clases pierden la cohesión, separalas en distintas clases.

### Aislarlas del cambio
Los requerimientos cambiarán, y por tanto el código lo hará de igual manera.
Podemos encontrar clases concretas que contienen detalles de implementación, y también clases abstractas que únicamente representan conceptos.
Podemos introducir interfaces y clases abstractas que nos ayuden a aislar nuestras clases del impacto de estos cambios (*E.g: Ports & adapters*).
