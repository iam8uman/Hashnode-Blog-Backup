---
title: "useReducer vs useState concept WHY and HOW ?"
seoTitle: "useReducer WHY & HOW?"
datePublished: Tue Jul 11 2023 11:24:07 GMT+0000 (Coordinated Universal Time)
cuid: cljy7fn60001u09mmenng0d7c
slug: usereducer-vs-usestate-concept-why-and-how
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689074543544/515e1b7d-a7ed-43c6-b71d-45f5d7c0d9bc.png
tags: usereducer, usestate, reacthooks, reactjs-development-services

---

```javascript
import { useReducer } from "react";

const initialState = 0;

const reduce = (state, action) => {
  switch (action) {
    case "Increment":
      return state + 1;
    case "Decrement":
      return state - 1;
    case "Reset":
      return initialState;

    default:
      return state;
  }
};

const Countreducerhook = () => {
  const [count, dispatch] = useReducer(reduce, initialState);

  return (
    <div className="border-2 border-blue-300 ">
      <div className="m-3 p-3 bg-purple-400 border-2 border--state-500 rounded-md text-2xl text-center">Count is  {count} </div>
      <div className="box flex justify-center m-5 p-3 ">
        <div className="m-3 p-3 bg-amber-400 border-2 border-purple-500 rounded-md text-2xl" onClick={() => dispatch("Increment")}>Increment</div>
        <div className="m-3 p-3 bg-amber-400 border-2 border-purple-500 rounded-md text-2xl" onClick={() => dispatch("Decrement")}>Decrement</div>
        <div className="m-3 p-3 bg-amber-400 border-2 border-purple-500 rounded-md text-2xl" onClick={() => dispatch("Reset")}>Reset</div>
      </div>
    </div>
  );
};

export default Countreducerhook;
```

## What did I learn from this EP18?

---

## useReducer()

* used for state management (wait what ? for state management we already have useState ?
    
* exactly it is an alternative of useState in better way.
    
* JS have reduce() method in array and imporoved version of this is the useReducer
    

## \-----------------------------

Not much but I just learned the concept of reduce methods in js and its replica on reactjs. Important 2 things

* **useReducer(reducer,initialState) // takes 2 parameter**
    
* **reducer(currentState,action) // which also takes 2 paramter**
    

useReducer returns 2 values i.e. newstate,dispatch

### Remember it is an alternative to useState for state management.

# \--------------------------

# What I learned from this EP19

step by step

1. useReducer(reducer,initialState) useReducer takes 2 parameter as an argument 1st one is reducer function( used in js) and 2nd one is initialState
    
2. initialState =0
    
3. now define reducer method reducer(state,action)
    

apply switch cases and display respective state value.

1. Remember useReducer hooks return 2 values i.e. \[newState, dispatch\] newState is the state returned from reducer method dispatch is a method which will rendor with the respective state
    

here we use onClicked={()=&gt;dispatch("Increment")} i.e. dispatch method renders the Increment state from the reducers method in the switch case.

@iam8uman