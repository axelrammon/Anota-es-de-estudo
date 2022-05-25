# Promises

uma Promise tem 3 estados
- Pending
- Fulfilled
- Rejected

## Estrutura

~~~javascript
  const myPromise = new Promise((resolve, reject) => {
    window.setTimeout(() => {
      resolve(console.log('Resolvida!'));
    }, 2000);
  });
~~~

## Manipulação

~~~javascript
  const myPromise = new Promise((resolve, reject) => {
    window.setTimeout(() => {
      resolve(console.log('Resolvida!'));
    }, 2000);
  });

  await myPromise
    .then((result) => result + 'passando pela then')
    .then((result) => result + 'e agora acabou')
    .catch((err) => console.log(err.message));
~~~