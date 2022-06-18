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

- 📝 A Typed superset of JavaScript
  ```ts
  const x: number = 10;
  const greet: string = "hello world";
  ```
- 🚀 Compiles to regular JavaScript
- 🎉 Developed and maintained by Microsoft

---

# What does it provide?

- 💥 Has a very powerful type system
- 🧪 Object-Oriented Programming
  - 🔧 Support for access modifiers
  - 📝 Abstract classes etc
- 💫 Adopts concepts from other languages
  - 📙 Namespace
  - 📦️ Interface
  - 💡 Generic
  - 🎨 Decorator
- 🧑‍💻 TypeScript feels simillar to C#
  - 🧐 Fun fact: C# and TypeScript is both designed by Anders Hejlsberg
- 🚨 Everything is a syntactic sugar

---

# Why does it matter?

### 🐛 Helps us find potential errors in compile-time

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

### 🧠 It leaves our intent in the code

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

### 🧑‍💻 Provides awesome Developer Experience (DX)

<br>

- 🐛 Reduces potential errors and improves productivity
- ✅ TypeScript provides a Language Server
  - 📦️ Comes with VSCode out of the box
  - 💡 We get better code completions and intellisense
- 🔨 Integrates well with other developer tools like ESLint etc
- 👽️ Fun Fact: VSCode is written in TypeScript

---

# Why does it matter?

### 🚀 TypeScript is Extremely Popular

<br>

- Most libraries and frameworks are written in TypeScript.

![]()

<img
  class="w-[600px] rounded"
  src="https://i.ibb.co/bgR6fg0/Screen-Shot-2022-05-22-at-10-13-37-PM.png"
/>

---

# TypeScript Compiler

A dive into TypeScript compilation process.

<div class="flex space-x-20 mt-10">
  <div class="w-56 h-24 border border-white flex items-center justify-center text-center px-6">
  You Code
  </div>
  
  <div class="w-56 h-24 border border-white flex items-center justify-center text-center px-6">
  Abstract Syntax Tree (AST)
  </div>
  <div class="w-56 h-24 border border-white flex items-center justify-center text-center px-6">
  Regular JavaScript
  </div>
</div>

<div class="ml-76 mt-16">
  <div class="w-56 h-24 border border-white flex items-center justify-center text-center px-6">
  typechecker
  </div>
</div>

<arrow v-click="1" x2="355" y2="200" x1="280" y1="200" color="#564" width="2" arrowSize="1" />

<arrow v-click="2" x2="450" y2="305" x1="450" y1="250" color="#564" width="2" arrowSize="1" />

<arrow v-click="3" x1="480" y1="305" x2="480" y2="250" color="#564" width="2" arrowSize="2" />

<arrow v-click="4" x2="660" y2="200" x1="585" y1="200" color="#564" width="2" arrowSize="1" />

<br> 
<br>

- Abstract Syntax Trees or ASTs are tree representations of code
- TypeChecker is a special program if verifies that your code is typesafe

---

# Configuring the TS Compiler

- A `tsconfig.json` file in a directory indicates that it is the root of a TypeScript project
- When we run tsc on the command line, it searches for a `tsconfig.json`
- Example `tsconfig.json`
  ```js
  {
    "compilerOptions": {
      "outDir": "dist",
      "target": "ES6",
      "module": "CommonJS",
      "noEmitOnError": true,
      "lib": ["DOM", "ESNext"],
    },
    "include": ["src"],
    "watchOptions": {
      "watchDirectory": "useFsEvents"
    }
  }
  ```
