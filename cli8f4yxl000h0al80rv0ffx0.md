---
title: "Fetch and Display data using API"
seoTitle: "Fetch and Display data using API"
seoDescription: "5 Simple Steps to Fetch and Display data using API"
datePublished: Mon May 29 2023 05:38:03 GMT+0000 (Coordinated Universal Time)
cuid: cli8f4yxl000h0al80rv0ffx0
slug: fetch-and-display-data-using-api
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1685338507411/0d9dac8c-7a02-4d5b-a21f-f72beb7f4e96.png
tags: apis, reactjs, rest-api, sumannn, fetchapi

---

In this blog post, we will delve into the process of fetching and presenting data using APIs within a React application. We will explore various approaches for data retrieval in React and guide you through each method. By leveraging APIs, we can retrieve data from servers and seamlessly showcase it in our application.

**API** stands for “Application Programming Interface,” which is a method of communication between different applications. For example, a news application contains regular news data, and the same data comes to the application with the help of APIs. There are various types of APIs, like the REST API, the GraphQL API, the SOAP API, etc.

**ReactJS** is an open-source library developed by Facebook used to create web applications’ user interfaces. It is a JavaScript-based library that consists of multiple extensions for the entire application.

With the help of React, we can create dynamic applications, as it needs less code and gives more functionality. Not only this, it also provides a dedicated tool for debugging the application to find errors or bugs.

As ReactJS is dynamic in nature, we can get the data using APIs and display it in our application.

To render some data in our front end, we either need a backend to store our data and then make use of the data, or we can simply use APIs to have some mock data while building an application.

When we use APIs, we don’t need a backend and are also not required to build anything from scratch. Mostly, we use the REST API or the GraphQL API to access the data added to the server.

---

## **How does an API work?**

The workings of an API are very easy to understand. Let’s understand it with an example. Say we want to build a new application and we don’t have our own backend. Now, to display the news in our application, we need some third-party APIs to access their backend server and display the data in our app.

Now, there are 3 things we must have noted, i.e., an application, a server, and an API. Most times, the API is in between the app and server because whenever the client requests the data, the API makes a GET request to the server and sends that back to the application for display.

---

## **Methods of fetching data using API**

We commonly use a Web API called REST, or Representational State Transfer API which consists of HTTP methods to fetch data from the server and display it in the application. A REST API has several methods, which are discussed further below: 

1. **GET:** This method is used to fetch the data from a server endpoint.
    
2. **POST:** This method is used to post the data to a server endpoint.
    
3. **DELETE:** This method is used to delete the data from a server endpoint.
    
4. **PUT:** This method is used to update or modify the data from a server endpoint.
    

Now as you have understood all the methods of the API, we can now move on to how the data is fetched from the server. To fetch the data, we use the **GET** method.

The different ways of Fetching the data in a React application are given below:

* Using React Hooks
    
* Using JavaScript Fetch API
    
* Using async/await
    
* Using Axios library
    
* Using React query
    

For now, we’ll only discuss the two ways of fetching data i.e., using **JavaScript Fetch API** and using **Axios library API**.

---

## **Using JavaScript Fetch API**

The JavaScript Fetch API is an inbuilt browser’s native API that gives an easy interface to fetch the data from the network. The simplest way to use fetch() is by taking one argument and the path from where the data is to be fetched and then returning a promise in a JSON object.

In this example, we are going to use mock data provided freely by [https://jsonplaceholder.typicode.com/](https://jsonplaceholder.typicode.com/) in JSON format. We are going to use the user’s endpoint from that API i.e., [https://jsonplaceholder.typicode.com/users](https://jsonplaceholder.typicode.com/users).

See the below steps to implement and use Fetch API to fetch the data in a react app.

---

### **Step 1. Create a react application**

```javascript
npx create-react-app demo
```

### **Step 2. Change your project directory**

```javascript
cd demo
```

### **Step 3. Access the API endpoint**

Now, as done in the above method 1, where we’ll also access the API endpoint and store it in a const variable so that we can use it anytime and anywhere.

```javascript
const url = “https://jsonplaceholder.typicode.com/users”;
```

### **Step 4. Import the useState() hook and set to hold data**

```javascript
import React, { useState } from 'react';

const [data, setData] = useState([])
```

### **Step 5. Create a FetchInfo() callback function to fetch and store data**

We will create a callback function that will store the user’s data and then use the useEffect() hook to make the function run every time the page loads. 

```javascript
const fetchInfo = () => { 
return fetch(url) 
        .then((res) => res.json()) 
        .then((d) => setData(d)) 
}

useEffect(() => {
	fetchInfo();
}, [])
```

Now your App.js file should Iook like below:

```javascript
import "./App.css";
import React, { useState, useEffect } from "react";

function App() {
  const url = "https://jsonplaceholder.typicode.com/users";
  const [data, setData] = useState([]);

  const fetchInfo = () => {
    return fetch(url)
      .then((res) => res.json())
      .then((d) => setData(d))
  }


  useEffect(() => {
    fetchInfo();
  }, []);

  return (
    <div className="App">
      <h1 style={{ color: "green" }}>using JavaScript inbuilt FETCH API</h1>
      <center>
        {data.map((dataObj, index) => {
          return (
            <div
              style={{
                width: "15em",
                backgroundColor: "#35D841",
                padding: 2,
                borderRadius: 10,
                marginBlock: 10,
              }}
            >
              <p style={{ fontSize: 20, color: 'white' }}>{dataObj.name}</p>
            </div>
          );
        })}
      </center>
    </div>
  );
}

export default App;
```

---

## **Using Axios Library**

Axios is an online HTTP library running on node.js that allows us to make various HTTP requests to a given server endpoint. If we see it working, then it uses the *http* module on the server side, whereas it uses *XMLHttpRequests on the* browser side. For this example, we are going to use the GET method to fetch and display the data in our React application. Here we don’t need to convert the result into a JSON object; it already comes as a JSON object.

See the below steps for the installation of the Axios library and the fetching process of the data in a react app.

---

### **Step 1. Create a react application**

The first thing to do is create a React application from scratch using the below npx command. Write or copy/paste the following to create a react app in your desired directory and name the project of your choice. For this example, we have created a project called “demo.”

```javascript
npx create-react-app demo
```

### **Step 2. Change your project directory**

Once the project is created, change the directory to where the app folder is created.

```javascript
cd demo
```

### **Step 4. Install the Axios library with npm or yarn**

For using the axios library, we need to install that and we can do that using two ways i.e., either install using NPM or Yarn. Install it with any one of your choice or requirements.

```javascript
npm install axios
```

Or

```javascript
yarn add axios
```

### **Step 5. Access the API endpoint**

Now, as done in the above method 1, where we’ll also access the API endpoint and store it in a const variable so that we can use it anytime and anywhere.

```javascript
const url = “https://jsonplaceholder.typicode.com/users”;
```

### **Step 6. Import the Axios and useState() hook and set to hold data**

Import the installed axios library to the App.js file and also the useState() hook to hold the data in a variable.

```javascript
import React, { useState } from 'react';
import axios from 'axios';

const [data, setData] = useState([])
```

### **Step 7. Create a FetchInfo() callback function to fetch and store data**

In this method also, we will create a callback function that will store the user’s data and then use the useEffect() hook to make the function run every time the page loads. 

```javascript
const fetchInfo = () => { 
  return axios.get(url) 
           .then((response) => setUser(response.data));
}

useEffect(() => { 
      fetchInfo(); 
}, [])
```

Now your App.js file should look like the below:

```javascript
import "./App.css";
import React, { useState, useEffect } from "react";
import axios from "axios";

function App() {
  const url = "https://jsonplaceholder.typicode.com/users";
  const [data, setData] = useState([]);

  const fetchInfo = () => {
    return axios.get(url).then((res) => setData(res.data));
  };

  useEffect(() => {
    fetchInfo();
  }, []);

  return (
    <div className="App">
      <h1 style={{ color: "green" }}>using Axios Library to Fetch Data</h1>
      <center>
        {data.map((dataObj, index) => {
          return (
            <div
              style={{
                width: "15em",
                backgroundColor: "#CD8FFD",
                padding: 2,
                borderRadius: 10,
                marginBlock: 10,
              }}
            >
              <p style={{ fontSize: 20, color: 'white' }}>{dataObj.name}</p>
            </div>
          );
        })}
      </center>
    </div>
  );
}

export default App;
```

---

## To Summarize,

This blog post provided valuable insights into utilizing an API to retrieve data within a React.js application. We aimed to enhance your comprehension of API functionality, data retrieval methods, and various approaches to fetching data via an API. Furthermore, we explored the utilization of the native JavaScript Fetch API for data retrieval, as well as the benefits of employing the Axios library as a superior alternative.

---

> "Happy Face, Happy Reader" -s2