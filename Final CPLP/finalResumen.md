## MT1 Resumen

#### Verdadero o Falso

Marque con una cruz las respuestas Faltas
- [ ] El R-Valor de un puntero es el L-Valor del objeto que quiere representar
- [ ] Un error de Tipo Sintáctico siempre provoca un error de tipo semántico
- [ ] Los errores de semántica estática se detectan cuando el programa pasa a ejecución

#### Pregunta

Lea el siguiente fragmento de texto sacado de un libro de un lenguaje de programación XX y diga qué caracteristica del mismo le hace pensar en alguno de los criterios de evaluación de lenguajes. Justifique la respuesta. Qué otro concepto podría tenerse en cuenta para evaluar este criterio?

```python
while True:
  try:
    x = int(input("Please enter a number: "))
    break
  except ValueError:
    print("Oops!  That was no valid number.  Try again...")
```

La sentencia **try** funciona de la siguiente manera.
- Primero, se ejecuta la cláusula **try** (el código entre las palabras reservadas **try** y **except**).
- Si no ocurre ninguna excepción, el bloque **except** se salta el resto de la cláusula. Luego termina la ejecución de la sentencia **try**.
- Si ocurre una excepción durante la ejecución de la clausula **try**, el resto de la cláusula se salta. Luego, si su tipo coincide con la excepción nombrada luego de la palabra reservada **except**, se ejecuta la cláusula **except**, y la ejecución continúa luego de la sentencia **try**.
- Si ocurre una excepción que no coincide con la excepción nombrada en la cláusula **except**, esta se pasa a la sentencia **try** más afuera; si no se encuentra nada que la maneje, es una excepción no manejada, y la ejecución se frena con un mensaje como los mostrados arriba.

#### Pregunta

<table><td>

```pascal
program ideaone;
...
var while:integer;
...
begin
...
  cad:="hola";
  while:=20/2;
  writeln(while,cad);
end.

```
</td><td></td></table>