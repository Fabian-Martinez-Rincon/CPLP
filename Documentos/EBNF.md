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

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">