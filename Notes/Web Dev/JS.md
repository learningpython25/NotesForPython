

* A **scripting language** used to make web pages interactive.
* Runs in the browser (client-side) but also used on servers (Node.js).
* Works with **HTML & CSS** to build dynamic UIs.

---

## 🔤 2. Variables

```js
let x = 10;    // Block-scoped
const y = 20;  // Constant
var z = 30;    // Function-scoped (legacy)
```

---

## ⚙️ 3. Data Types

* **Primitive**: `String`, `Number`, `Boolean`, `null`, `undefined`, `Symbol`, `BigInt`
* **Objects**: Arrays, Functions, Objects

---

## 🔁 4. Control Structures

```js
if (x > 0) { ... }
else if (...) { ... }
else { ... }

for (let i = 0; i < 5; i++) { ... }

while (condition) { ... }

switch (value) {
  case 'a': ...; break;
  default: ...
}
```

---

## 🧮 5. Functions

```js
function add(a, b) {
  return a + b;
}

const sub = (a, b) => a - b; // Arrow function
```

---

## 🧱 6. Arrays & Objects

```js
let arr = [1, 2, 3];
arr.push(4); // [1,2,3,4]

let obj = { name: "Alice", age: 25 };
console.log(obj.name); // Dot notation
```

---

## 🔄 7. Looping Arrays

```js
arr.forEach(item => console.log(item));
let doubled = arr.map(x => x * 2);
let filtered = arr.filter(x => x > 1);
```

---

## 🧪 8. Comparison

* `==` checks value, **type coercion**
* `===` checks value and type (strict equality)

```js
"5" == 5     // true
"5" === 5    // false
```

---

## 🌐 9. DOM Manipulation

```js
document.getElementById("id");
document.querySelector(".class");

element.innerText = "Hello";
element.style.color = "red";
```

---

## 🕸 10. Events

```js
button.addEventListener("click", function() {
  alert("Clicked!");
});
```

---

## 🌈 11. ES6+ Features

* **Destructuring**: `let {a, b} = obj;`
* **Spread**: `let newArr = [...arr];`
* **Template Literals**: `Hello, ${name}`
* **Promises & async/await**

---

## ⚠️ 12. Hoisting & Scope

* `var` is hoisted; `let` & `const` are block-scoped.
* Functions are hoisted too.

---

## 📦 13. JSON & Fetch

```js
fetch('api/data.json')
  .then(res => res.json())
  .then(data => console.log(data));
```

