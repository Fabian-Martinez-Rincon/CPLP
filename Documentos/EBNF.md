<h1 align="center"> 🧠 EBNF
</h1>

- [Asterisco *](#asterisco)
- [Interrogación ?](#interrogación)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Asterisco *

El asterisco (*) en EBNF (Extended Backus-Naur Form) se utiliza para denotar la repetición cero o más veces de un elemento en una gramática.

```
<frase> ::= <palabra>*
```


Esto significa que la regla de producción `<frase>` se puede construir a partir de cero o más repeticiones de la regla de producción `<palabra>`. En otras palabras, una `<frase>` puede ser una sola `<palabra>` o una secuencia de varias `<palabras>`.

Otro ejemplo sería la regla de producción:

```
<expresión> ::= <número> (<operador> <número>)*
```

Esto indica que una `<expresión>` se puede construir a partir de un `<número>` seguido de cero o más repeticiones de un `<operador>` seguido de otro `<número>`. Por lo tanto, una expresión podría ser simplemente un número o una serie de operaciones matemáticas que involucran varios números y operadores.

En resumen, el asterisco (*) en EBNF se utiliza para indicar la repetición cero o más veces de un elemento en una gramática.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Interrogación ?

El signo de pregunta (?) en EBNF (Extended Backus-Naur Form) se utiliza para denotar la repetición cero o una vez de un elemento en una gramática.

Por ejemplo, si tenemos la regla de producción:

```
<nombre> ::= <primer-nombre> <apellido>?
```

Esto significa que un `<nombre>` se compone siempre de un `<primer-nombre>` seguido opcionalmente de un `<apellido>`. Si la regla de producción fuera así:

```
<nombre> ::= <primer-nombre> <apellido>*
```

En este caso, el signo de asterisco indicaría que un `<nombre>` puede tener cero o más `<apellido>`, lo cual no tendría mucho sentido en este contexto.

Otro ejemplo podría ser la regla de producción:



```
<elemento> ::= <etiqueta> (<atributo>)*
```

Esto indica que un `<elemento>` se compone de una `<etiqueta>` seguida opcionalmente de cero o más repeticiones de un `<atributo>`. En otras palabras, un `<elemento>` puede tener cero o más `<atributo>`, pero siempre tendrá al menos una `<etiqueta>`.

En resumen, el signo de pregunta (?) en EBNF se utiliza para indicar la repetición cero o una vez de un elemento en una gramática.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Suma +

En EBNF (Extended Backus-Naur Form), el símbolo de suma (+) se utiliza para denotar la repetición una o más veces de un elemento en una gramática.

Por ejemplo, si tenemos la regla de producción:

```
<secuencia> ::= <elemento>+
```

Esto significa que una `<secuencia>` debe tener al menos un `<elemento>`, pero también puede tener varios elementos repetidos. En otras palabras, una secuencia es una lista de uno o más elementos.

Otro ejemplo podría ser la regla de producción:

```
<expresión> ::= <número> | <expresión> <operador> <expresión>
```


En este caso, la barra vertical (|) representa una alternativa, es decir, `<expresión>` puede ser un `<número>` o una expresión que involucra dos expresiones unidas por un operador. La suma (+) se utiliza en la segunda alternativa para indicar que una expresión puede contener varios términos separados por operadores, como en una expresión matemática.

En resumen, el símbolo de suma (+) en EBNF se utiliza para indicar la repetición una o más veces de un elemento en una gramática

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">