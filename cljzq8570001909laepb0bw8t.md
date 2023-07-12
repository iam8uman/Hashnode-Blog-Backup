---
title: "Data Fetching using useReducer( )   ||   Why useReducer over useState hook ? SIMPLE    but  
  IMP*"
seoTitle: "Data Fetching using useReducer( ) || Why useReducer over useState?"
seoDescription: "useReducer over useState which one best? Why and how to use hooks?
Data Fetching using useReducer( ) || Why useReducer over useState hook ? SIMPLE  But IMP"
datePublished: Wed Jul 12 2023 12:57:56 GMT+0000 (Coordinated Universal Time)
cuid: cljzq8570001909laepb0bw8t
slug: data-fetching-using-usereducer-why-usereducer-over-usestate-hook-simple-but-imp
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689166500162/512c0d4c-8aad-429b-94f0-aa02292da424.png
tags: reactjs, usereducer, usestate, reacthooks, iam8uman

---

### Here in the case of useState we need to define every state for each useState like this.

```javascript
  const [load, setLoad] = useState(true);
  const [err, setErr] = useState("");
  const [post, setPost] = useState({}); 
```

And we should update the whole code like this

```javascript
import { useEffect, useState } from "react";
import axios from "axios";

const Datafetching = () => {
  const [load, setLoad] = useState(true);
  const [err, setErr] = useState("");
  const [post, setPost] = useState({});

  useEffect(() => {
    axios
      .get("https://jsonplaceholder.typicode.com/posts/1")
      .then((res) => {
        setLoad(false);
        setPost(res.data);
        setErr("Kaisa error hey yar ye toh");
        console.log(res.data);
      })
      .catch((error) => {
        setLoad(true);
        setPost({});
        setErr(error);
      });
  }, []);
  return (
    <>
      <h1 className="text-3xl text-slate-800 bg-slate-300">

        {load ? "loading" : post.title}
        {err ? err : null}

      </h1>
    </>
  );
};

export default Datafetching;
```

---

### But in the case of useReducer ( ) we can include whole this stuff into a single useReducer or more specifically into the reducer( ) method.

```javascript
const initialState = {
  Loading: true,
  post: {},
  error: "",
};
```

And the setup for useReducer like this here we define when the state changes for eg. when action changes into "FETCH\_SUCCESS" then this values changes accordingly and in the case of "FETCH\_FAILS" then responds accordingly.

```javascript
const reducer = (state = initialState, action) => {
  switch (action.type) {
    case "FETCH_SUCCESS":
      return {
        Loading: false,
        post: action.payload,
        error: "",
      };

    case "FETCH_FAILS":
      return {
        Loading: false,
        post: {},
        error: "Something went wrong !",
      };

    default:
      return state;
  }
};
```

### And whole code looks like this in the case of useReducer hook.

```javascript
import  { useEffect, useReducer } from "react";
import axios from "axios";

const initialState = {
  Loading: true,
  post: {},
  error: "",
};

const reducer = (state = initialState, action) => {
  switch (action.type) {
    case "FETCH_SUCCESS":
      return {
        Loading: false,
        post: action.payload,
        error: "",
      };

    case "FETCH_FAILS":
      return {
        Loading: false,
        post: {},
        error: "Something went wrong !",
      };

    default:
      return state;
  }
};

function DataFetchTwo() {
  const [state, dispach] = useReducer(reducer, initialState);

  useEffect(() => {
    axios
      .get("https://jsonplaceholder.typicode.com/posts/1")
      .then((res) => {
        dispach({ type: "FETCH_SUCCESS", payload: res.data });
      })
      .catch((error) => {
        dispach({ type: "FETCH_FAILS" });
        console.log(error)
      });
  }, []);

  return (
    <div>
      <h1 className="text-3xl text-slate-800 bg-slate-300">
        {state.Loading ? "loading" : state.post.title}
        {state.error ? state.error : null}
      </h1>
    </div>
  );
}

export default DataFetchTwo;
```

---

### Summary:)

1. In case of useState we need multiple useState for multiple state
    
2. But in the case of useReducer we can include all of these state into a initialState and just update accordingly.
    
3. REMEMBER useReducer is modification over useState
    

> Happy Face, Happy Reader - @iam8uman