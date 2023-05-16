---
title: 'Typescript in js files'
pubDate: 'May 13, 2023'
heroImage: '/typescript.png'
---
## Introduction to Using TypeScript Comments in JavaScript Files

TypeScript is a superset of JavaScript that introduces static typing and other advanced features to the JavaScript ecosystem. While TypeScript is typically used with dedicated .ts files, it is also possible to leverage its features within regular JavaScript files by utilizing TypeScript comments.

TypeScript comments allow developers to annotate JavaScript code with type information and take advantage of TypeScript's static analysis capabilities, even in files with a .js extension. These comments are used to provide type hints to the TypeScript compiler, enabling the detection of potential errors and improved tooling support.

By incorporating TypeScript comments in JavaScript files, developers can gradually introduce static typing and other TypeScript-specific features into their projects without the need for a full migration. This flexibility allows for a smoother transition from JavaScript to TypeScript, as developers can adopt TypeScript gradually, file by file or module by module, without disrupting the existing codebase.

```javascript
// @ts-check

/** @type{(a: number, b: number) => Promise<number>} */
async function area(a, b) {
  return a * b
}

let result = area("!,", 2) // ❌ ERR
result = area(1, 2)
console.log(result + 1) // ❌ ERR
```

In this guide, we will explore the usage of TypeScript comments in JavaScript files, highlighting how they can enhance code quality, improve development productivity, and provide a stepping stone for a more comprehensive adoption of TypeScript in your project.

reference: [typescriptlang/jsdoc](https://www.typescriptlang.org/docs/handbook/jsdoc-supported-types.html)

```javascript
// @ts-check

/**
@typedef {{
  name: string
  age: number
}} User
*/

/** @type{(b: User) => Promise<boolean>} */
export async function isUserBelow21(b) {
  return b.age < 21
}

let result = isUserBelow21("")
result = isUserBelow21({ name: "alice", age: 22 })
if (isUserBelow21({ name: "bob", age: 21 })) {
  console.log('Welcome!')
}
```
