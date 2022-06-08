## Renderização condicional

- Variáveis de elementos
- if inline com o operador lógico &&
- if-else inline com o operador condicional
- Evitando que um componente seja renderizado

#### Variáveis de elementos

~~~javascript
  const buttonA = <button>Primeiro btn</button>;
  const buttonB = <button>Segundo btn</button>;

  function App() {
    return (
      <div>
        <p>Digital</p>
        <p>Welcome</p>
        {buttonA}
        {buttonB}
      </div>
    );
  }
  export default App;
~~~

#### if inline com o operador lógico &&

~~~javascript
  const buttonA = <button>Histórico</button>;

  const hasCustomer = false;

  function App() {
    return (
      <div>
        <p>Digital</p>
        <p>Welcome</p>

        // AQUI ESTÁ O IF INLINE COM OPERADOR LÓGICO 
        {hasCustomer && (
          <div>
            Clique no botão para visualizar o Histórico
            <br />
            {buttonA}
          </div>
        )}
      </div>
    );
  }
~~~

#### if-else inline com o operador condicional

~~~javascript
  const buttonA = <button>Histórico</button>;
  const buttonB = <button>Cadastrar</button>;

  const hasCustomer = false;

  function App() {
    return (
      <div>
        <p>Digital</p>
        <p>Welcome</p>
        {hasCustomer ? (
          <div>
            Clique no botão para visualizar o Histórico
            <br />
            {buttonA}
          </div>
        ) : (
          <div>
            Clique para cadastrar cliente
            <br />
            {buttonB}
          </div>
        )}
      </div>
    );
  }
~~~

~~~javascript
  const buttonA = <button>Histórico</button>;
const buttonB = <button>Cadastrar</button>;

const hasCustomer = true;

function App() { 
  const renderShowHistory = () => (
    <div>
      Clique no botão para visualizar o Histórico
      <br />
      {buttonA}
    </div>
  )
  const renderAddCustomer = () => (
    <div>
      Clique para cadastrar cliente
      <br />
      {buttonB}
    </div>
  )
  return (
    <div>
      <p>Digital</p>
      <p>Welcome</p>
      {hasCustomer ? renderShowHistory() : renderAddCustomer()}
    </div>
  );
}
~~~

#### Evitando que um componente seja renderizado

~~~javascript

  const hasCustomer = true;

  function App() {
    
    const showCustomer = () => {
      if (!hasCustomer) return null

      return(
        <div>
          <h1>Nome cliente: Axel</h1>
        </div>
      )
    }

    return (
      <div>
        <div>
          {showCustomer()}
        </div>
      </div>
    );
  }
~~~