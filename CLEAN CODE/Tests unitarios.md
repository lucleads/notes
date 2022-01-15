# Las tres leyes del [TDD](https://www.guru99.com/test-driven-development.html)

### Primera ley
> ***"No debes escribir ningún código de producción a menos que haga pasar un test unitario que falle"***

Tiene que existir un test que describe un aspecto nuevo del comportamiento de la unidad que estamos desarrollando, por tanto el test en producción debería fallar si no existe el nuevo código.

### Segunda ley
> ***"No debes escribir más de un test unitario del que sea suficiente para fallar; y los errores de compilación son fallos"***

Esto significa que se debe comenzar con el test más simple que compruebe el comportamiento de la nueva feature, y este en un principio debe fallar.
Hay que recordar que cuando hablamos de TDD escribimos primero el test, y a continuación el código que aplica la funcionalidad, por tanto normalmente el primer fallo del test será una excepción por *función no encontrada*.

### Tercera ley
> ***"No debes escribir más código de producción del que sea necesario para hacer pasar un test unitario que falle"***

El TDD se basa en desarrollar los tests que requiere la nueva funcionalidad y hacer el desarrollo en función de estos tests, por lo que no debería ser necesario escribir más código del necesario para pasar este test.

# Consejos
Los tests se deben mantener tán limpios, como el código de producción, y no deben convertirse en un actor secundario del desarrollo, ya que el mantenimiento y buen funcionamiento de estos tests, es tan importante como el funcionamiento del propio código.

##### Un *assert* por test
Cada función de un test unitario debería contener únicamente una afirmación de *assert*.
Aunque esta no es una norma estricta, siempre debemos tratar de reducir el número de asserts en cada test para exclarecer la finalidad del test.
De esta forma, debemos minimizar el número de *asserts* por concepto, y hacer que cada función de test compruebe únicamente un concepto.