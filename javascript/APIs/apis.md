# APIS

## fetch

*Consumindo APIs*

~~~javascript
  fetch(url, options)
    .then(response => response.json())
    .then(json => console.log(json))

  // Retorna uma Promise
~~~

## Operações no banco

### Get

~~~javascript
  fetch('https://endereco.api.com/', {
    method: 'GET',
    cache: 'no-cache',
  })
    .then(response => response.json())
    .then(json => console.log(json))

  // Retorna uma Promise
~~~

### Post

~~~javascript
  fetch('https://endereco.api.com/', {
    method: 'POST',
    cache: 'no-cache',
    body: JSON.stringfy(data),
  })
    .then(response => response.json())
    .then(json => console.log(json))

  // Retorna uma Promise
~~~
