# Objectos y estructuras de datos
Hay un motivo para mantener las variables como `private`. No queremos que nadie más dependa de ellas. Queremos mantener la libertad de cambiar su tipo/implementación sin miedo a los efectos colaterales.

### Diferencia entre objetos y estructuras de datos
El código procedimental (código utilizado en estructuras de datos) facilita añadir funciones sin modificar la estructura de datos. Por otro lado, el código orientado a objetos facilita añadir clases sin modificar las funciones existentes.

### Data transfer objects
La forma más básica de representar una estructura de datos, es una clase con variables públicas y sin métodos. Esta estructura se suele llamar *Data Transfer Object* o **DTO**.

### Active Record
Los *Active Record* son una forma especial de DTOs. Normalmente contienen métodos como `save` o `find`.


Las estructuras de datos se encargan de exponer información, y no tienen un comportamiento significativo.