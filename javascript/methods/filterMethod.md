# Filter Method

- cria um novo array

## Sintaxe

~~~javascript
  array.filter(callback, thisArg);
~~~

~~~javascript
  const frutas = ['maçã fuji', 'maçã verde', 'laranja', 'abacaxi'];

  frutas.filter((fruta) => fruta.includes('maçã'));

  // retorno: ['maçã fuji', 'maçã verde']
~~~