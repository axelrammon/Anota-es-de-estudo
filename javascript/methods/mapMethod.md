# Map Method

- cria um novo array;
- Não modifica o array original;
- Realiza operações em ordem;

## Sintaxe

~~~javascript
  array.map(callback, thisArg);
  callback(item, index, array);
~~~

**Callback:** função a ser executada em cada elemento
**thisArg (opcional):** valor de 'this' dentro da função de callback

## Map vs forEach

~~~javascript
  // Usando map

  const array = [1, 2, 3, 4, 5];

  array.map((item) => item * 2});
  // retorno: [2, 4, 6, 8, 10]

  // Usando forEach

  const array = [1, 2, 3, 4, 5];

  array.forEach((item) => item * 2});
  // retorno: undefined

~~~