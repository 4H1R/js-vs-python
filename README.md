## 1. Syntax

**Python**

- **General Characteristics:**

  - **Indentation-Based:** Uses indentation to define code blocks.

  - **Whitespace Significant:** Proper indentation is crucial.

  - **Readable and Clean:** Emphasizes readability.

- **Example:**

```python
def greet(name):
    if name:
        print(f"Hello, {name}!")
    else:
        print("Hello, World!")

greet("Alice")
```

**JavaScript**

- **General Characteristics:**

  - **Brace-Based:** Uses curly braces `{}` to define code blocks.

  - **Semicolons Optional:** Though not required, semicolons can be used to terminate statements.

  - **Flexible Syntax:** More flexibility with code structure.

- **Example:**

```javascript
function greet(name) {
  if (name) {
    console.log(`Hello, ${name}!`);
  } else {
    console.log('Hello, World!');
  }
}

greet('Alice');
```

---

## 2. Memory Management and How It Works Under the Hood

**Python**

- **Automatic Memory Management:**

  - **Garbage Collection:** Uses reference counting and a cyclic garbage collector to manage memory.

  - **Memory Allocation:** Handled by Python’s memory manager, abstracting complexity from the developer.

- **Under the Hood:**

  - **Reference Counting:** Keeps track of the number of references to each object.

  - **Cycle Detection:** Identifies and collects objects that reference each other, preventing memory leaks.
    **JavaScript**

- **Automatic Memory Management:**

  - **Garbage Collection:** Primarily uses mark-and-sweep algorithms.

  - **Memory Allocation:** Managed by the JavaScript engine (e.g., V8), abstracting complexity from the developer.

- **Under the Hood:**

  - **Mark-and-Sweep:** Periodically scans memory to identify and collect unused objects.

  - **Generational Collection:** Optimizes garbage collection by categorizing objects based on their lifespan.

---

## 3. Types of Data with Examples and Syntax

**Python**

- **Primitive Types:**
  - **Integer:** `int`

```python
age = 30
```

- **Float:** `float`

```python
pi = 3.14159
```

- **String:** `str`

```python
name = "Alice"
```

- **Boolean:** `bool`

```python
is_active = True
```

- **Composite Types:**
  - **List:** Ordered, mutable collection

```python
fruits = ["apple", "banana", "cherry"]
```

- **Tuple:** Ordered, immutable collection

```python
coordinates = (10, 20)
```

- **Dictionary:** Key-value pairs

```python
person = {"name": "Alice", "age": 30}
```

- **Set:** Unordered, unique elements

```python
unique_numbers = {1, 2, 3}
```

**JavaScript**

- **Primitive Types:**
  - **Number:** Represents both integers and floats

```javascript
let age = 30;
let pi = 3.14159;
```

- **String:** `string`

```javascript
let name = 'Alice';
```

- **Boolean:** `boolean`

```javascript
let isActive = true;
```

- **Undefined:** `undefined`

```javascript
let data;
```

- **Null:** `null`

```javascript
let empty = null;
```

- **Symbol:** Unique and immutable

```javascript
let sym = Symbol('unique');
```

- **Composite Types:**
  - **Object:** Key-value pairs

```javascript
let person = { name: 'Alice', age: 30 };
```

- **Array:** Ordered collection

```javascript
let fruits = ['apple', 'banana', 'cherry'];
```

- **Function:** First-class objects

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

---

## 4. Syntax of Basic Constructs with Examples and Syntax

**Python** **If Statement**

```python
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")
```

**Loops**

- **For Loop:**

```python
for i in range(5):
    print(i)
```

- **While Loop:**

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

**Functions**

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
```

**Lists**

```python
fruits = ["apple", "banana", "cherry"]
print(fruits[0])  # Output: apple
```

**Objects (Dictionaries)**

```python
person = {"name": "Alice", "age": 30}
print(person["name"])  # Output: Alice
```

---

**JavaScript** **If Statement**

```javascript
let x = 10;
if (x > 5) {
  console.log('x is greater than 5');
} else if (x === 5) {
  console.log('x is equal to 5');
} else {
  console.log('x is less than 5');
}
```

**Loops**

- **For Loop:**

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

- **While Loop:**

```javascript
let count = 0;
while (count < 5) {
  console.log(count);
  count++;
}
```

**Functions**

```javascript
function add(a, b) {
  return a + b;
}

let result = add(3, 5);
console.log(result); // Output: 8
```

**Arrays**

```javascript
let fruits = ['apple', 'banana', 'cherry'];
console.log(fruits[0]); // Output: apple
```

**Objects**

```javascript
let person = { name: 'Alice', age: 30 };
console.log(person.name); // Output: Alice
```

---

## 5. Float Numbers and How They're Saved in Memory with Examples and Syntax

**Python**

- **Float Representation:**

  - **Double Precision:** Python’s `float` type uses double-precision (64-bit) IEEE 754 format.

  - **Storage:** Consists of sign bit, exponent, and mantissa.

- **Example:**

```python
pi = 3.141592653589793
print(pi)  # Output: 3.141592653589793
```

- **Memory Storage:**

  - Internally stored as binary fractions.

  - Limited precision can lead to rounding errors.

```python
print(0.1 + 0.2)  # Output: 0.30000000000000004
```

**JavaScript**

- **Float Representation:**

  - **Double Precision:** JavaScript’s `Number` type also uses double-precision (64-bit) IEEE 754 format.

  - **Storage:** Similar structure with sign bit, exponent, and mantissa.

- **Example:**

```javascript
let pi = 3.141592653589793;
console.log(pi); // Output: 3.141592653589793
```

- **Memory Storage:**

  - Internally stored as binary fractions.

  - Limited precision can lead to rounding errors.

```javascript
console.log(0.1 + 0.2); // Output: 0.30000000000000004
```

---

## 6. Types of Functions with Examples and Syntax

**Python**

- **Function Types:**
  - **Standard Functions:**

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!
```

- **Lambda Functions (Anonymous Functions):**

```python
add = lambda a, b: a + b
print(add(3, 5))  # Output: 8
```

- **Higher-Order Functions:**

```python
def apply_function(func, value):
    return func(value)

def square(x):
    return x * x

print(apply_function(square, 4))  # Output: 16
```

- **Generator Functions:**

```python
def count_up_to(max):
    count = 1
    while count <= max:
        yield count
        count += 1

counter = count_up_to(5)
for num in counter:
    print(num)
# Output: 1 2 3 4 5
```

**JavaScript**

- **Function Types:**
  - **Function Declarations:**

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet('Alice')); // Output: Hello, Alice!
```

- **Function Expressions:**

```javascript
const add = function (a, b) {
  return a + b;
};

console.log(add(3, 5)); // Output: 8
```

- **Arrow Functions:**

```javascript
const multiply = (a, b) => a * b;
console.log(multiply(3, 5)); // Output: 15
```

- **Higher-Order Functions:**

```javascript
function applyFunction(func, value) {
  return func(value);
}

function square(x) {
  return x * x;
}

console.log(applyFunction(square, 4)); // Output: 16
```

- **Generator Functions:**

```javascript
function* countUpTo(max) {
  let count = 1;
  while (count <= max) {
    yield count;
    count++;
  }
}

const counter = countUpTo(5);
for (let num of counter) {
  console.log(num);
}
// Output: 1 2 3 4 5
```

---

## 7. OOP and Inheritance with Examples and Syntax

**Python**

- **Class Definition and Inheritance:**

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

dog = Dog("Buddy")
cat = Cat("Whiskers")

print(dog.speak())  # Output: Buddy says Woof!
print(cat.speak())  # Output: Whiskers says Meow!
```

- **Key Points:**

  - **Inheritance:** Use parentheses to inherit from a parent class.

  - **Method Overriding:** Subclasses can override methods of the parent class.

  - **`super()` Function:** To call methods from the parent class.

- **Class Definition and Inheritance (ES6 Syntax):**

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    // To be overridden by subclasses
  }
}

class Dog extends Animal {
  speak() {
    return `${this.name} says Woof!`;
  }
}

class Cat extends Animal {
  speak() {
    return `${this.name} says Meow!`;
  }
}

const dog = new Dog('Buddy');
const cat = new Cat('Whiskers');

console.log(dog.speak()); // Output: Buddy says Woof!
console.log(cat.speak()); // Output: Whiskers says Meow!
```

- **Key Points:**

  - **Inheritance:** Use `extends` keyword to inherit from a parent class.

  - **Method Overriding:** Subclasses can override methods of the parent class.

  - **`super()` Function:** To call the constructor or methods from the parent class.

---

## Summary Table

| Topic             | Python                                                                                                               | JavaScript                                                                                                                                         |
| ----------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Syntax            | Indentation-based, readableExample:python<br>def greet(name):<br> print(f"Hello, {name}!")<br>                       | Brace-based, flexibleExample:javascript<br>function greet(name) {<br> console.log(`Hello, ${name}!`);<br>}<br>                                     |
| Memory Management | Automatic with reference counting and garbage collector                                                              | Automatic with mark-and-sweep and generational collection                                                                                          |
| Data Types        | int, float, str, bool, list, tuple, dict, setExample:python<br>age = 30<br>                                          | Number, String, Boolean, Undefined, Null, Symbol, Object, ArrayExample:javascript<br>let age = 30;<br>                                             |
| Basic Constructs  | if, for, while, def, list, dictExample:python<br>if x > 5:<br> print(x)<br>                                          | if, for, while, function, array, objectExample:javascript<br>if (x > 5) {<br> console.log(x);<br>}<br>                                             |
| Floats            | Double-precision (float)Example:python<br>pi = 3.14<br>                                                              | Double-precision (Number)Example:javascript<br>let pi = 3.14;<br>                                                                                  |
| Functions         | Standard, lambda, higher-order, generatorsExample:python<br>def add(a, b):<br> return a + b<br>                      | Function declarations, expressions, arrow functions, higher-order, generatorsExample:javascript<br>function add(a, b) {<br> return a + b;<br>}<br> |
| OOP & Inheritance | class, inheritance using parenthesesExample:python<br>class Dog(Animal):<br> def speak(self):<br> return "Woof!"<br> | class, extends keywordExample:javascript<br>class Dog extends Animal {<br> speak() {<br> return "Woof!";<br> }<br>}<br>                            |

---

This comparison covers the fundamental aspects of Python and JavaScript across various programming concepts. Make sure to practice writing and understanding code in both languages to solidify your understanding for the exam. Good luck!
