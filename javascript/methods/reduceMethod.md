# Reduce Method

- Executa uma função em todos os elementos do array, retornando um valor único

## Sintaxe

~~~javascript
  array.reduce(callbackFn, initialValue);
~~~

**Callback:** função a ser executada a partir do acumulador
**initialValue:** valor sobre o qual o retorno final irá atuar

Ex.:

~~~javascript
  const callbackFn = function(accumulator, currentValue, index, array) {
    // do something
  }

  callbackFn.reduce(callbackFn, initialValue);
~~~

**Accumulator/prevValue:** Acumulador de todas as chamadas de callbackFn

**currentValue:** Elemento atual sendo acessado pela função