# Async / await

*funcões assíncronas precisam dessas duas palavras*

~~~javascript
  async function resolvePromise() {
    const myPromise = new Promise((resolve, reject) => {
      window.setTimeout(() => {
        resolve('Resolvida');
      }, 3000);
    });

    const resolved = await myPromise
      .then((result) => result + ' passando pelo then');
      .then((result) => result + ' e agora acabou!');
      .catch((err) => console.log(err.message));

    return resolved;
  }
~~~

*Precisa dar um **await resolvePromise()***

~~~javascript
  async function resolvePromise() {
    const myPromise = new Promise((resolve, reject) => {
      window.setTimeout(() => {
        resolve('Resolvida');
      }, 3000);
    });

    let result;

    try {
      result = await myPromise
        .then((result) => result + ' passando pelo then');
        .then((result) => result + ' e agora acabou!');
    } catch(err) {
      result = err.message;
    }

    return resolved;
  }
~~~