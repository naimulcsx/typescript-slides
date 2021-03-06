---
theme: ./theme
class: text-center
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
title: Learning TypeScript
---

# TypeScript

TypeScript for JavaScript Developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <!-- <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button> -->
  <a href="https://github.com/naimulcsx/typescript-in-bangla" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---

# What is TypeScript?

- ๐ A Typed superset of JavaScript
  ```ts
  const x: number = 10;
  const greet: string = "hello world";
  ```
- ๐ฝ๏ธ Types are optional
- ๐ Compiles to regular JavaScript
- ๐ Developed and maintained by Microsoft

---

# What does it provide?

- ๐ฅ Has a very powerful type system
- ๐งช Object-Oriented Programming
  - ๐ง Support for access modifiers
  - ๐ Abstract classes etc
- ๐ซ Adopts concepts from other languages
  - ๐ Namespaces
  - ๐ฆ๏ธ Interfaces
  - ๐ก Generics
  - ๐จ Decorators
- ๐งโ๐ป TypeScript feels like the result of adding parts of C# to JavaScript
  - ๐ง Fun fact: C# and TypeScript is both designed by Anders Hejlsberg
- ๐จ Remember: Everything is a syntactic sugar

---

# Why does it matter?

### ๐ Helps us find potential errors in compile-time

<br>

```js {1-5|6}
const user = {
  firstName: "Naimul",
  lastName: "Haque",
  role: "Software Engineer",
};
console.log(user.name);
```

<arrow v-click="2" x1="360" y1="300" x2="240" y2="260" color="#564" width="2" arrowSize="1" />

<br>
<br>

<p class="text-red-500" v-click>Property 'name' does not exist on type '{ firstName: string; lastName: string; role: string; }'.</p>

---

# Why does it matter?

### ๐ง? It leaves our intent in the code

<br>

- JavaScript
  ```js
  function add(a, b) {
    return a + b;
  }
  ```
  - Anyone can literally call this function with any kind of value.
- TypeScript
  ```ts
  function add(a: number, b: number): number {
    return a + b;
  }
  ```
  - A function that expects two numbers as parameters and returns a number.

---

# Why does it matter?

### ๐งโ๐ป Provides awesome Developer Experience (DX)

<br>

- ๐ Reduces potential errors and improves productivity
- โ TypeScript provides a Language Server
  - ๐ฆ๏ธ Comes with VSCode out of the box
  - ๐ก We get better code completions and intellisense
- ๐จ Integrates well with other developer tools like ESLint etc
- ๐ฝ๏ธ Fun Fact: VSCode is written in TypeScript

---

# Why does it matter?

### ๐ TypeScript is Extremely Popular

<br>

- Most libraries and frameworks are written in TypeScript.

![]()

<img
  class="w-[600px] rounded"
  src="https://i.ibb.co/bgR6fg0/Screen-Shot-2022-05-22-at-10-13-37-PM.png"
/>
