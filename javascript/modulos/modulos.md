# Módulos

- Arquivos javascript que tem a capacidade de exportar e importar informações de outros arquivos do mesmo tipo
- Módulos sempre estão em "strict mode";
- Podem ser utilizadas em extensões .js e .mjs
- Para testes locais, é necessário utilizar um servidor
- Ao importar utilizar "./" antes

Vantagens

- Organização do código
- Compartilhamento de variáveis e escopos diferentes
- Explicita as dependências dos arquivos

## Exportar

### Named exports

~~~javascript
  export function mostrarIdade(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.idade}`;
  }

  export function mostrarCidade(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.cidade}`;
  }

  export function mostrarHobby(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.hobby}`;
  }
~~~

~~~javascript
  function mostrarIdade(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.idade}`;
  }

  function mostrarCidade(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.cidade}`;
  }

  function mostrarHobby(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.hobby}`;
  }

  export {
    mostrarIdade,
    mostrarCidade,
    mostrarHobby
  }
~~~

### Default exports

- Só pode haver um por arquivo
- Será o retorno padrão do seu arquivo

~~~javascript
  function mostrarIdade(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.idade}`;
  }

  function mostrarCidade(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.cidade}`;
  }

  function mostrarHobby(pessoa) {
    return `A idade de ${pessoa.nome} é ${pessoa.hobby}`;
  }

  export {
    mostrarIdade,
    mostrarCidade
  }

  export default mostraHobby;
~~~

## Importar

### Named Exports

~~~javascript
  import {funcao, variavel, classe} from './arquivo.js'
~~~

### Default exports

~~~javascript
  import valorDefault from './arquivo.js'
~~~

## Trocando nome de import

~~~javascript
  import { arquivo as Apelido } from './arquivo.js';

  Apelido.metodo();
~~~

## Importando todos os dados de um arquivo

~~~javascript
  import * as INFOS from './arquivo.js';

  INFOS.metodoA();
  console.log(INFOS.variaveis)
~~~

## Vinculando ao HTML

~~~html
  <script type="module" src="./main.js"></script>
~~~