---
title: "Day 21 of #100daysofcode: Context API"
seoTitle: "What is Context API then?

Context API is used to pass global variable"
seoDescription: "Day 21 of #100daysofcode: Context API"
datePublished: Sun Oct 15 2023 07:35:10 GMT+0000 (Coordinated Universal Time)
cuid: clnr5izk4000k08l08fmt77vk
slug: day-21-of-100daysofcode-context-api
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697351011962/eac84566-cbc9-4f0a-a497-5f9eb2e80071.png
tags: apis, reactjs, context-api, iam8uman, whysumancode

---

---

### What is Context API then?

Context API is **<mark>used to pass global variables anywhere in the code.</mark>** It helps when there is a need for a sharing state between many nested components.

`In the below image. When we have to send a card title from the Dashboard component to the card component without passing it through that intermediate component then Context API is useful.`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697349891443/1536e9ae-0301-4e60-9288-2b348816c51e.png align="center")

It is light in weight and easier to use, to create a context need to call <mark>React.createContext().</mark>

```javascript
import React from 'react'

const userContext= React.createContext();

export default userContext
```

<mark>There is no need to install other dependencies or third-party libraries like redux for state management.</mark>

---

### Why is context API used? |&| When to use?

Context API solves the problem of `prop drilling in React. Prop Drilling occurs when data is to be passed between multiple layers before finally sending it to the required component. This makes the application slower. This problem is solved by Context API` as it creates global variables to be used throughout the application without any middle components involved. It is also easier to use than React-Redux.

---

### Working of Context API

To work with Context API we need ***<mark>React.createContext</mark>***. It has two properties <mark>Provider and Consumer</mark>. <mark>The Provider acts as a parent it passes the state to its children whereas the Consumer uses the state that has been passed.</mark>

---

### Benefits of Context API over React-Redux

* In Redux we have to manipulate or update multiple files to add even a single feature but in Context, it can be done in much fewer lines of code
    
* <mark>One way data binding in React is maintained using Context whereas Redux violates it.</mark>
    
* Multiple stores/contexts can be created using Context whereas Redux creates just a single store
    
* <mark>We don't have to install third-party dependencies like Redux.</mark>
    

---

> `"The success you are looking for, is in the work that you are avoiding!" -Modern Wishdom Podcast`
> 
> Feel free to contact- @[Suman Sharma](@iam8uman)