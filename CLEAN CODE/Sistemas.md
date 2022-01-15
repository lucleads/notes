# Sistemas

### Separación del *Main*
Una forma de mantener la separación entre la forma de construir nuestras clases y su función, es mover todos los aspectos de como se construye esta clase a una capa superior o *main*, o a módulos que son llamados por esta clase, y asumir en el resto de nuestro programa, que estos objectos se construyen e instancian de forma adecuada.
Esto implica que la dirección de las dependencias va siempre en contra del *main*, por lo que la aplicación es agnóstica la clase *main*, o el proceso de instanciación.

### Inyección de dependencias
Un mecanismo apropiado para separar el proceso de construcción de la función de las clases, es la [*Inyección de Dependencias](https://www.campusmvp.es/recursos/post/que-es-la-inyeccion-de-dependencias-y-como-funciona.aspx)*(*Dependency Injection* - DI), la aplicación práctica de la [*Inversión de Control*](https://www.raona.com/introduccion-inversion-control/)(*Inversion of Control* - IoC) al gestor de dependencias. 

> **Robert C. Martin:** Una arquitectura de sistema óptima consiste en modularizar los dominios según su ámbito de actuación, cada uno de los cuales se implementa con *Plain Old Java* (u otros) *Objecs*. Los diferentes dominios se integran sin invadir el ámbito de actuación de otros dominios, utilizando *Aspects* o *Aspects-like tools*. Esta arquitectura puede estar dirigida por tests, al igual que el código.

Cuando estemos diseñando sistemas o módulos, no debemos olvidar elegir siempre la opción más simple de implementar, que puede realizar de forma óptima la tarea requerida.