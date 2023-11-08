---
title: "Static & Dynamic Typed Language! Typescript's Need?"
seoTitle: "Static & Dynamic Typed Language! Typescript's Need? sourceMap: True;"
seoDescription: "Static & Dynamic Typed Language! Typescript's Need? sourceMap: True; for fix issues and debug. Sitemap.xml"
datePublished: Wed Nov 08 2023 15:24:29 GMT+0000 (Coordinated Universal Time)
cuid: clopwuz4d000909lcdiy5c00f
slug: static-dynamic-typed-language-typescripts-need
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699456840674/ceb81cad-9e27-42a5-a803-b4ea4a5f4eee.png
tags: seo, typescript, sitemap, whysumancode, static-and-dynamic-typed-language

---

---

### Static type Language: C, C++, C##

First, we have the type of variable, and then this remains the same for the entire program.

```cpp
int a=5;
a="Suman" // Not Possible
```

---

### Dynamically Typed Language: Javascript, Python, Ruby.

The type of variables can be changed dynamically like this,

```javascript
let a=5;
a="Suman"; // Valid
Math.random(a); // Not possible
```

This actually creates a problem, initially, a is an integer but later on its type changed into a string. Due to the dynamic nature of such language, it is possible but if we test some functionality on the same variable considering it as an integer creates issues.

`( yesari code garda whole program crash hune chance panii hunxa, that's why TYPESCRIPT is needed. Typescript le Static type checking provide garxa! )`

<mark>Typescript: Javascript with Type Checking!</mark>

```typescript
let x: number =10;
x = "suman"; // Error
```

`Compiler le nai Error Show garxa typescript ma, So that Error aaune possibility ne ekdam kam hunxa. That's why Microsoft introduced Typescript.`

---

### Debug & fixed issues in vs-code.

For debugging typescript code in vs-code, you need to enable `sourceMap: True;`  
which lets you debug the issues that are present in the code.

The debug section has this `lunch.json` which you can use & add this line which I commented on below.

```json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "node",
            "request": "launch",
            "name": "Launch Program",
            "skipFiles": [
                "<node_internals>/**"
            ],
            "program": "${workspaceFolder}\\typescript\\src\\index.ts",
            "preLaunchTask": "tsc: build - tsconfig.json", // add this 
            "outFiles": [
                "${workspaceFolder}/**/*.js"
            ]
        }
    ]
}
```

---

### Sitemap Generate for SEO | Upload this sitemap.xml file

Currently, I have two domains, one for a blog site i.e. sumansharma07.com.np, and the other for my portfolio in sumansharma.info.np.

---

### Sitemap Generator :

It is used to generate the .XML file for the given URLs. In my case, I want to update my sitemap so that it ranks in the Search engine