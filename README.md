### OOP nima?

Object-Oriented Programming **class** va **obyektlar**ga asoslangan dasturlash stili. Dasturdagi hamma ma’lumotlar object va classlar ko’rinishida bo’ladi. JavaScript esa prototypelarga asoslangan, **procedural** til hisoblanadi. Ya’niki, u funksional va object-oriented stillarning ikkalasini ham qo’llab quvvatlaydi.

### Class nima?

Class bu objectlar uchun ishlatilinadigan **shablon**. Class bir xil property va methodlarga ega bo’lgan objectlardan foydalanishning oson yo’lidir. Ya’ni murakkab objectlarning strukturasini qurishda va ulardan keyinchalik ham foydalanishda classlardan foydalanamiz.

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(
      `Hello, my name is ${this.name} and I am ${this.age} years old.`
    );
  }
}

const jane = new Person("Jane", 25);

jane.sayHello();
```

Tepadagi misol kabi yangi class yaratmoqchi bo’lganimizda har doim `class` keywordidan foydalanishimiz kerak bo’ladi. `constructor` orqali esa class qabul qiladigan barcha o’zgaruvchilarni kiritib olamiz. Shu classdan andoza olib, yangi object create qilishimiz uchun esa `new` keywordidan foydalanishimiz kerak bo’ladi.

<hr>

### OOP dagi prinsiplar

OOP da asosan 4 ta prinsip mavjud:

<ul>
    <li><a href="./encapsulation/README.md">Polymorphism</a></li>
    <li><a href="#">Inheritance</a></li>
    <li><a href="#">Encapsulation</a></li>
    <li><a href="#">Abstraction</a></li>
</ul>
