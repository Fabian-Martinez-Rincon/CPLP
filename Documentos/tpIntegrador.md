<h2 align="center"> CONCEPTOS Y PARADIGMAS DE LENGUAJES DE PROGRAMACIÓN
TRABAJO INTEGRADOR 2023

</h2>

### Grupo 27 (Python/JavaScript)
- Fabian Martinez Rincon 18153/1
- Iñaki Agustin Lapeyre 19508/3
- Luciano Ariel Lopez 14994/0





<details> <summary> IMPORTANTE: </summary>

<br>

La entrega de cada parte del trabajo es obligatoria se debe realizar únicamente en un archivo pdf, el cual debe contener las siguientes partes:


- `1)` Una carátula (una carilla) con el nombre y legajo de cada uno de los integrantes del grupo que hayan participado del trabajo, el número de grupo asignado por la cátedra y los lenguajes asignados; así como la bibliografía consultada. No se puede referenciar wikipedia. Las referencias deben ser de páginas oficiales del lenguaje, de libros, de manuales del lenguaje, de documentación de cátedras de enseñanza del lenguaje, de papers/artículos, entre otros.
- `2)` El enunciado y desarrollo de la tarea pedida (código fuente incluido).
- `3)` El archivo entregado debe tener el siguiente nombre ParteNgrupoXX.pdf (respetar este formato de nombre) donde N es el número de Parte y XX representa el nro. de grupo asignado por la cátedra. Sólo debe ser subido a la plataforma por un integrante del grupo que hayan participado del trabajo y debe respetar la extensión de páginas máxima indicada en el trabajo con fuente Arial 11 para el contenido de cada una de ambas entregas (SIN EXCEPCION, íncluida la carátula). Pautas del Trabajo Integrador:
    - Los grupos estarán conformados por 4 personas sin excepción.
    - En caso de que un alumno quede como único integrante de grupo debe comunicarlo a los JTP para ser reasignado a otro grupo.
    - Se debe entregar en forma obligatoria las dos entregas del Trabajo Integrador.
    - La segunda entrega deberá contener las correcciones de la primera (en caso de haberla desaprobado) en el mismo documento entregado.
    - Cada grupo tendrá asignado un lenguaje Principal y uno secundario y un ayudante y día de la práctica. El ayudante sólo asistirá y responderá consultas sin ser obligatorio remitirse a la práctica y ayudante asignado para disipar dudas. Sin embargo se recomienda contactar con el ayudante para tener una mejor respuesta.
    - En el transcurso de la cursada se llamará a coloquio a cada grupo en el día asignado para realizar preguntas sobre el trabajo integrador. Esta nota (entre otras) servirá para determinar la nota final del alumno.

</details>




<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

- [A) Escriba fragmentos de código de mínimo 5 y máximo 10 líneas de extensión](#a)
- [B) Cite ejemplos de código (mínimo 5, máximo 15 líneas) en ambos lenguajes](#b)
- [C) Cite un ejemplo de código (5 líneas mínimo, 10 líneas máximo) para cada](#c)
- [D) Defina un ejemplo de código (5 líneas mínimo,15 líneas máximo) en cada](#d)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

Considerando los lenguajes asignados a su grupo, resuelva cada uno de los puntos del
enunciado.

1era Parte (Fecha Final de entrega: viernes 21/04/2023). EXTENSIÓN MÁXIMA 6
PÁGINAS incluyendo la portada.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## `Ejercicio A)` 
Escriba fragmentos de código de mínimo 5 y máximo 10 líneas de extensión que permitan ejemplificar al menos tres criterios de evaluación en los lenguajes asignados. Puede citar un ejemplo para cada criterio elegido y compararlo entre los lenguajes, colocando una breve descripción textual para cada uno.

---

### Simplicidad y legibilidad:
Básicamente es la forma en la que el lenguaje está diseñado para ser fácil de leer/entender

`Python`
```python
def calcular_media(lista):
    suma = 0
    for num in lista:
        suma += num
    media = suma / len(lista)
    return media

numeros = [2, 4, 6, 8, 10]
media = calcular_media(numeros)
print("La media es:", media)
```


Este código muestra cómo calcular la media de una lista de números en Python utilizando una función. La sintaxis es clara y fácil de entender, con el uso de nombres de variables descriptivos y una indentación adecuada para las estructuras de control.

`JavaScript`
```javascript
function calcularMedia(lista) {
  let suma = 0;
  for (let i = 0; i < lista.length; i++) {
    suma += lista[i];
  }
  let media = suma / lista.length;
  return media;
}
let numeros = [2, 4, 6, 8, 10];
let media = calcularMedia(numeros);
console.log("La media es:", media);
```

Este código muestra cómo calcular la media de una lista de números en JavaScript utilizando una función personalizada. La sintaxis es sencilla y utiliza nombres de variables descriptivos, aunque la estructura de control es un poco más detallada que en Python

---


### Confiabilidad

Podemos ilustrar la confiabilidad de estos lenguajes con su manejo de excepciones

#### Python
Tiene un sistema integrado de manejo de excepciones que permite detectar y manejar errores de manera segura. El siguiente fragmento de código muestra cómo capturar una excepción y manejarla de manera adecuada:

```python 
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("No se puede dividir entre cero")
```

Javascript
En JavaScript, se pueden manejar excepciones utilizando el bloque try...catch. Este bloque permite envolver el código que puede generar una excepción en un bloque try, y luego manejar la excepción en un bloque catch que se ejecutará si se produce una excepción. El bloque try contiene el código que se ejecutará normalmente, mientras que el bloque catch contiene el código que se ejecutará en caso de que se produzca una excepción.

	try {
 	   let resultado = 10 / 0 
}
catch (error) {
  	  console.log("No se puede dividir entre cero")
}

Comparación Python y Javascript en confiabilidad:
Tanto Python como JavaScript tienen mecanismos integrados para el manejo de excepciones, aunque con algunas diferencias en su sintaxis y funcionamiento.
En ambos se pone el código/operación que puede generar una excepción en el bloque try{...} y en caso de producirse se corta y se salta directamente al bloque de código contenido dentro de except, en caso de python, o catch, en caso de Javascript. Se pueden manejar múltiples excepciones en ambos y ejecutar un código dependiendo de la excepción capturada.
Ambos lenguajes permiten el uso de la cláusula finally para definir un bloque de código que siempre se ejecutará, independientemente de si se produce una excepción o no.


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## `Ejercicio B)`
Cite ejemplos de código (mínimo 5, máximo 15 líneas) en ambos lenguajes asignados que permitan analizar A NIVEL SINTÁCTICO 4 estructuras de control de manera comparada entre los lenguajes asignados. Coloque una breve descripción a cada ejemplo.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## `Ejercicio C)`
Cite un ejemplo de código (5 líneas mínimo, 10 líneas máximo) para cada lenguaje asignado donde pueda distinguirse con claridad chequeos de semántica estática y dinámica a la hora de ejecutar/interpretar código. Debe poder entenderse con claridad, más allá de la naturaleza del lenguaje, distintos tipos de errores que se controlan y el momento en que dichos chequeos se realizan hasta poder ejecutar propiamente el programa.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## `Ejercicio D)`
Defina un ejemplo de código (5 líneas mínimo,15 líneas máximo) en cada lenguaje seleccionado donde se visualicen los distintos tipos de variables que soporta el lenguaje en cuanto al tiempo de vida, y realice una tabla donde se sitúen todos los identificadores junto con los valores de sus atributos tal como se vió en la práctica correspondiente.


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">