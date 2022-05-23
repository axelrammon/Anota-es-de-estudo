## SET()
*(Coleções chaveadas)*

*Sets são estruturas que armazenam apenas **valores únicos***

### Set vs Array

- Possui valores únicos;
- Em vez da propriedade length, consulta-se o número de registros pela propriedade size;
- Não possui os métodos map, filter, reduce etc.

Exemplo: 

  ~~~javascript
    const myArray = [1, 2, 3, 4, 4, 5, 3, 2, 3];

    const mySet = new Set(myArray);

    // Set(5) {1, 2, 3, 4, 5}
  ~~~

  ~~~javascript
    const mySet = new Set();

    mySet.add(1);
    mySet.add(3);

    mySet.has(1);
    // true

    mySet.has(2);
    // false

    mySet.size;
    // Tamanho do Set

    mySet.delete(3);
  ~~~