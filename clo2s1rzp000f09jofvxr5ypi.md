---
title: "Redux | Redux-Toolkit (RTK) | React-redux | Auto Prefixer."
seoTitle: "Redux | Redux-Toolkit (RTK) | React-redux | Auto Prefixer."
seoDescription: "Redux | Redux-Toolkit (RTK) | React-redux | Auto Prefixer.
Day26 of #100daysofcode- @iam8uman"
datePublished: Mon Oct 23 2023 10:51:06 GMT+0000 (Coordinated Universal Time)
cuid: clo2s1rzp000f09jofvxr5ypi
slug: redux-redux-toolkit-rtk-react-redux-auto-prefixer
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697710579493/72053aa0-be85-447b-8004-00aec1cbf4a5.png
tags: reactjs, redux, redux-toolkit, whysumancode, auto-prefixer

---

### **What is Redux?**

Redux is a <mark>state management library</mark> that allows you to manage the state of your JavaScript applications more efficiently and predictably.

1. ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697699815202/f3a0cbe8-2647-4cda-9098-c2bdc2de629c.webp align="center")
    
2. If you are building a house then instead of keeping each and every detail inside of your head you prefer to keep these details in the paper or something similar.  
    Redux works similarly by keeping track of your application's state in a single place called the "<mark>store</mark>."
    
    Let's say you're building an e-commerce site. You may need to keep track of the items in a user's cart, their payment information, and their shipping details.  
    SAME as in ContextAPI,
    
    <mark>Instead of passing this information from component to component using props, Redux allows you to store them in </mark> `one central location` <mark>where they can be easily accessed and updated. This makes it easier to manage complex states and keep your application organized.</mark>
    
    `Note: Redux is not for only react but for all JS frameworks.`  
    The key components that enable this centralized approach to state management are:
    
    1. Store
        
    2. Actions
        
    3. Dispatch
        
    4. Reducers
        
        ### **Store**
        
        The Redux store is like a <mark>giant container </mark> that holds all the data for your application.
        
        ### **Actions (**`what to do?`**)**
        
        An action is <mark>an </mark> `object` <mark>that describes what changes need to be made to the state of your application.</mark> It sends data from your application to the Redux store and serves as the only way to update the store.
        
        ### **Dispatch (**`Distribute the action`**)**
        
        In Redux, <mark>dispatch is a</mark> `function` <mark>provided by the store that allows you to send an action to update the state of your application.</mark> When you call `dispatch`, the store runs an action through all of the available reducers, which in turn updates the state accordingly. --------------------  
        **(Dispatch le** `reducers` **ko use garera** `state` **lai update garxa)**
        
        ### **Reducers**
        
        In Redux, <mark>a reducer is a</mark> `function` <mark>that takes in the current state of an application and an action as arguments and returns a new state based on the action.</mark>
        

---

### React-Redux

First of all, **Redux** is an independent library for state management in web development. React-redux is specially designed for state management in <mark>React.js.</mark>

---

### **Redux-toolkit**

Redux Toolkit is like a handy toolkit that makes managing the data in your web applications easier, especially when you have a lot of data or many parts of your app that need to share data.

Imagine your app's data is like a jigsaw puzzle. You have lots of pieces (data) that need to fit together correctly. Redux Toolkit provides you with tools to organize and connect these pieces effortlessly.

Here's how it simplifies things:

1. **<mark>Store</mark>**<mark>:</mark> Redux Toolkit gives you a special place called the "store" to keep all your data. It's like a big box where you neatly organize your puzzle pieces.
    
2. **<mark>Reducers</mark>**: It helps you create "reducers" that are like puzzle-solving instructions. Reducers tell your app how to change the data when something happens, like a user clicking a button.
    
3. **<mark>Actions</mark>**<mark>:</mark> You can create "actions" that are like notes to your app. When a button is clicked, you send a note (action) to the store, and the store uses the reducer to make the puzzle pieces fit together correctly.
    
4. **<mark>Slices</mark>**: Redux Toolkit even lets you organize your data into "slices." Each slice is like a section of your puzzle, making it easier to work with specific parts of your app.
    

So, Redux Toolkit is like the magic toolbox that makes it simpler to manage, update, and use data in your web app. It's great for larger apps where keeping everything in order can be a bit like solving a big jigsaw puzzle

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697709627720/befdbc02-93d6-4a16-a9b3-ecc8af1e66ef.png align="center")

---

### <mark>Installation</mark> of redux-toolkit

### An Existing App[​](https://redux-toolkit.js.org/introduction/getting-started#an-existing-app)

Redux Toolkit is available as a package on NPM for use with a module bundler or in a Node application:

* npm
    
* yarn
    

```javascript
npm install @reduxjs/toolkit
```

If you need React bindings:

```javascript
npm install react-redux
```

---

### Useful APIs in Redux-toolkit

* [`configureStore()`](https://redux-toolkit.js.org/api/configureStore):
    
* [`createReducer()`](https://redux-toolkit.js.org/api/createReducer):
    
* [`createAction()`](https://redux-toolkit.js.org/api/createAction):
    
* [`createSlice()`](https://redux-toolkit.js.org/api/createSlice):
    
* [`createAsyncThunk`](https://redux-toolkit.js.org/api/createAsyncThunk):
    
* [`createEntityAdapter`](https://redux-toolkit.js.org/api/createEntityAdapter):
    
* [`createSelector`](https://redux-toolkit.js.org/api/createSelector):
    

---

### Auto-Prefixer

It is a web platform that is used to convert your CSS code compatible with all browsers. Initially,, you write CSS for only one browser but later we must check its validity in all browsers that's why auto-prefixer is used.

Generally, Auto-Prefixer is used when the whole program or code is written.

---

> "If you are going through HELL, keep going....  
> Why did you stop at hell?" Keep doing & only you can do it!