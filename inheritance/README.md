### Inheritance nimani anglatadi?

  <img src="./inhertiance-image.jpg" style="width: 100%;">

Inheritance bu ma'lum bir classning boshqa bir classga parent element sifatida rol o'ynab, unga o'zida bor bo'lgan strukturani to'liqligicha yoki ma'lum miqdorda **meros** sifatida o'tkazish demakdir. Ya'ni dasturlashda objectlar o'zidagi strukturani boshqa bir objectdan inherit qilib olish imkoniyatiga ham egadirlar. Bu tamoyil classlar orasida o'zaro <a href="https://dev.to/manomite/what-is-hierarchy-in-programming-5f7o">hierarchical</a> ko'rinishidagi bog'liqlikni ta'minlaydi.

Asosan 4 turdagi inheritance mavjud:

#### 1. Single inheritance

Bu turda child class faqatgina bitta class strukturasidan inherit oladi.

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  eat() {
    console.log(`${this.name} is eating.`);
  }
}

class Dog extends Animal {
  bark() {
    console.log(`${this.name} is barking.`);
  }
}

const dog = new Dog("Max");
dog.eat(); // Inherited from the parent class
dog.bark(); // Defined in the child class
```

#### 2. Multiple inheritance

Bu bir classning bir vaqtning o'zida bir nechta classdan inherit olish tushuniladigan inheritance turidir. JavaScript tabiiy, sof multiple inheritanceni support qilmasa-da, shu funksionallik boshqacha syntax orqali amalga oshiriladi.

```javascript
class Swimmer {
  swim() {
    console.log(`${this.name} is swimming.`);
  }
}

class Singer {
  sing() {
    console.log(`${this.name} is singing.`);
  }
}

class Performer {}

Object.assign(Performer.prototype, Swimmer.prototype, Singer.prototype);

const performer = new Performer();
performer.swim(); // Mixed in from the Swimmer class
performer.sing(); // Mixed in from the Singer class
```

Bu misolda `Performer` classi to'g'ridan to'g'ri `Swimmer` va `Singer` classlaridan inherit olmasdan, `Object.assign` methodi orqali ikkala classning `prototype`ni aralashtirib o'zining prototypega qo'shib oldi.

#### 3. Multi-level inheritance

Qachonki classning inherit olgan parent classi ham o'zi aslida boshqa bir classdan inherit olgan bo'lsa, bu inheritance turiga Multi-level inheritance deyiladi.

```javascript
class Vehicle {
  startEngine() {
    console.log("Engine started.");
  }
}

class Car extends Vehicle {
  drive() {
    console.log("Car is being driven.");
  }
}

class SportsCar extends Car {
  accelerate() {
    console.log("Sports car is accelerating.");
  }
}

const sportsCar = new SportsCar();
sportsCar.startEngine(); // Inherited from the grandparent class
sportsCar.drive(); // Inherited from the parent class
sportsCar.accelerate(); // Defined in the child class
```

#### 4. Hierarchical Inheritance

Bir nechta classlar bitta umumiy parentdan inherit olishsa, ularning inherit turiga Hierarchical inheritance deyiladi

```javascript
class Shape {
  constructor(color) {
    this.color = color;
  }

  draw() {
    console.log(`Drawing a shape with color ${this.color}.`);
  }
}

class Circle extends Shape {
  draw() {
    console.log(`Drawing a circle with color ${this.color}.`);
  }
}

class Rectangle extends Shape {
  draw() {
    console.log(`Drawing a rectangle with color ${this.color}.`);
  }
}

const circle = new Circle("red");
const rectangle = new Rectangle("blue");

circle.draw(); // Inherited from the parent class
rectangle.draw(); // Inherited from the parent class
```
