
##Variables and Data Types

```ts
let isDone: boolean = false;
let age: number = 25;
let firstName: string = "John";
let bigNumber: bigint = 100n;
let notSure: any = "Can be anything";
```

### Arrays
```ts
let numbers: number[] = [1, 2, 3, 4, 5];
let strings: Array<string> = ["one", "two", "three"];
```

### Tuples (Fixed-length arrays)
```ts
let person: [string, number] = ["John", 25];
```

### Enums
```ts
enum Color {
  Red,   // 0
  Green, // 1
  Blue   // 2
}
let myColor: Color = Color.Green;
console.log(myColor); // Output: 1
```

---

## Functions
```ts
function add(a: number, b: number): number {
  return a + b;
}
console.log(add(3, 5)); // Output: 8
```

### Optional and Default Parameters
```ts
function greet(name: string, greeting: string = "Hello"): string {
  return `${greeting}, ${name}`;
}
console.log(greet("John")); // Output: Hello, John
console.log(greet("John", "Hi")); // Output: Hi, John
```

### Arrow Functions
```ts
const multiply = (x: number, y: number): number => x * y;
console.log(multiply(4, 5)); // Output: 20
```

---

##  Objects and Interfaces
### Defining Objects
```ts
let user: { name: string; age: number } = {
  name: "John",
  age: 25,
};
```

### Using Interfaces
```ts
interface User {
  name: string;
  age: number;
}

let person1: User = { name: "John", age: 25 };
```

---

##  Classes and Objects
### Basic Class
```ts
class Car {
  brand: string;
  
  constructor(brand: string) {
    this.brand = brand;
  }

  showBrand(): void {
    console.log(`This car is a ${this.brand}`);
  }
}

let myCar = new Car("Toyota");
myCar.showBrand(); // Output: This car is a Toyota
```

### Access Modifiers
- `public`: Accessible anywhere
- `private`: Accessible only within the class
- `protected`: Accessible within the class and subclasses

```ts
class Person {
  public name: string;
  private age: number;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }

  getAge(): number {
    return this.age;
  }
}

let person2 = new Person("John", 25);
console.log(person2.name); // Allowed
console.log(person2.getAge()); // Allowed
// console.log(person2.age); // Error: age is private
```


