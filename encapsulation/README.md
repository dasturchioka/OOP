### Encapsulation nimani anglatadi?

Dasturlashda Encapsulation <i>(yoki inkapsulyatsiya)</i> classlarga bir xil umumiylikga ega bo'lgan property va methodlarni joylashtirish tushuniladi. Inkapsulyatsiya ortidagi asosiy g'oya objectning ichki holatiga **to'g'ridan-to'g'ri kirishni cheklash** va aniq belgilangan interfeyslar orqali boshqariladigan kirishni ta'minlashdir. Bu tamoyil ma'lumotlar yaxlitligiga, kod modulligiga va <a href="#">abstraktsiyaga</a> erishishga yordam beradi.

Inkapsulyatsiya object ichidagi ma'lumotlarning to'g'ridan to'g'ri ochiq holatda qolib ketmasligini, faqatgina maxsus va shu objectning ichida mavjud bo'lgan methodlar orqaligina undan foydalana olish xususiyatini ta'minlaydi. Bu o'zgaruvchilardan ruxsatsiz foydalanishni cheklashga yordam beradi.

JavaScript-da inkapsulyatsiyani `class` yordamida va `public` va `private` kabi access modifikatorlaridan foydalanish orqali ko'rsatish mumkin:

```javascript
class Person {
  #name; // Private member

  constructor(name) {
    this.#name = name; // Private property
  }

  #privateMethod() {
    // Private method
    console.log("This is a private method");
  }

  getName() {
    // Public method
    return this.#name;
  }
}

const person = new Person("John");
console.log(person.getName()); // Accessing public method
console.log(person.#name); // Error: Cannot access private member
person.#privateMethod(); // Error: Cannot access private method
```
Bu misolda `#name` propertysi va `#privateMethod` methodi maxfiy, ya'ni ulardan faqatgina `Person` classi ichidagina foydalanishimiz mumkin. `getName` methodi esa private ma'lumotlarga umumiy kirish nuqta rolini bajarib beradi.
