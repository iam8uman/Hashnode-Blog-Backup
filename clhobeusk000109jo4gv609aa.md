---
title: "The ES7 extension provides beneficial React code snippets for use in VS Code."
seoTitle: "ES7 extension provides beneficial React code snippets for use in VS"
seoDescription: "The ES7 extension provides beneficial React code snippets for use in VS Code."
datePublished: Mon May 15 2023 03:58:22 GMT+0000 (Coordinated Universal Time)
cuid: clhobeusk000109jo4gv609aa
slug: the-es7-extension-provides-beneficial-react-code-snippets-for-use-in-vs-code
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684122944056/6695cd85-2ebc-49a7-b1e0-3dd7ccb27637.png
tags: es7, reactjs, sumannn, reactjs-snippets, react-snippets

---

While exploring React, I realized that crafting the fundamental code for developing fresh components in my application was becoming tiresome and repetitive. Whenever a new component was created, the identical import code, component function code, export default, and so on needed to be added.

One fine day, while struggling to understand the notion of state, a fellow member of my group shared a YouTube video that explained React in a two-hour crash course (provided in the [link](https://www.youtube.com/watch?v=w7ejDZ8SWv8)).

This video introduced me to the incredible VS Code extension known as **ES7 React/Redux/React-Native/JS** snippets. These snippets aid in expediting workflow and act as shortcuts by enabling us to enter a few letters, which then generate the code we frequently use in our React applications.

The snippets offered by this extension assist us in reducing the time spent on writing the basic code and allow us to concentrate more on the actual functionality.

This blog provides a short list of useful snippets with examples of their various outputs. The exhaustive list & how to install this extension can be found [here](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets).

## 1\. imr

```javascript
import React from 'react';
```

## 2\. imrse

```javascript
import React, { useState, useEffect } from 'react';
```

## 3\. imp(import)

```javascript
import moduleName from 'module';
```

## 4\. imd(import restructured)

```javascript
import {  } from 'module';
```

## 5\. clg

```javascript
console.log(object);
```

## 6\. rfc(react functional component)

```javascript
import React from 'react'

export default function App() {
  return (
    <div>
      
    </div>
  )
}
```

## 7\. rfce(react functional component w/ export default at the bottom)

```javascript
import React from 'react'

function App() {
  return (
    <div>
      
    </div>
  )
}

export default App;
```

## 8\. rafce(react component utilizing an arrow function)

```javascript
import React from 'react'

const App = () => {
  return (
    <div>
      
    </div>
  )
}

export default App
```

## 9\. nfn(named arrow function)

```javascript
const name = (params) => {
  
}
```

## 10\. imrr

```javascript
import { BrowserRouter as Router, Route, NavLink} from 'react-router-dom';
```

Some other snippets:  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684122210169/5c39afcb-9a90-4baa-9aa4-0a70e1b59368.png align="center")

There are many more, You can check it out. I have given the link to the respective path.

> "Happy Face, Happy Reader"-s2