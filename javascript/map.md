## MAP()
*(Coleções chaveadas)*

- Coleção de arrays no formato [chave, valor]
- pode ser iterado por um loop for...of

### Maps vs Objeto
- Maps podem ter chaves de qualquer tipo;
- Maps possuem a propriedade length;
- Maps são mais fáceis de iterar;
- Utilizado quando o valor das chaves é desconhecido;
- Os valores tem o mesmo tipo;


Exemplo: 

  ~~~javascript
    const myArray = [1, 2, 3, 4, 4, 5, 3, 2, 3];

    const myMap = new Map(myArray);

    // [1, 2, 3, 4, 4, 5, 3, 2, 3]
  ~~~

  ~~~javascript
    const myMap = new Map();

    myMap.set('apple', 'fruit');
    // Map(1) {"apple" => "fruit"}

    myMap.get(apple);
    // "fruit"

    myMap.delete("apple");
  ~~~