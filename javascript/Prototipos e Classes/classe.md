# Classe

*__Syntatic sugar__ Uma sintaxe feita para facilitar a escrita*

*Não possui classe nativamente. Todas as classes são objetos e a herança se dá por protótipos.*

~~~javascript
  class Meal {
    constructor (food) {
      this.food = food
    }

    eat() {
      return 'emoji'
    }
  }
~~~

*Exemplo com GETTERS e SETTERS*

~~~javascript
  class Animal {
    constructor (type = 'animal') {
      this.type = type
    }

    get type() {
      return this._type
    }

    set type(val) {
      this._type = val.toUpperCase()
    }
    
    makeSound() {
      console.log('Making animal sound')
    }
  }

  let a = new Animal()
  console.log(a.type) // ANIMAL
  
~~~

*SUPER*

~~~javascript
  class Cat extends Animal {
    constructor() {
      super('cat')
    }
    
    makeSound() {
      super.makeSound()
      console.log('Meow')
    }
  }

  let b = new Cat()
  console.log(b.type) // CAT

~~~