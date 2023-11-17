---
title: "Next.js- Data Fetching-SSR, SSG, ISR, Error Handling, Loading, Caching Data, API-endpoints"
seoTitle: "Next.js- Data Fetching-SSR, SSG, ISR, Error Handling, Loading, Caching"
seoDescription: "Next.js- Data Fetching-SSR, SSG, ISR, Error Handling, Loading, Caching Data, API-endpoints"
datePublished: Fri Nov 17 2023 13:20:37 GMT+0000 (Coordinated Universal Time)
cuid: clp2necgu000c09js6hptgg15
slug: nextjs-data-fetching-ssr-ssg-isr-error-handling-loading-caching-data-api-endpoints
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700226853986/69e38430-98f7-400d-be13-9582d88deca4.png
tags: error-handling, nextjs, full-stack-development, whysumancode, routets

---

### Data Fetching in Next.js!

1. Server Side Rendering.
    
2. Static Site Generation.
    
3. Incremental Static Generation.
    

---

### Error Handling in Next.js!

For error Handling, we can have `error.js/tsx/jsx` a file that automatically handles errors in the Next.js application.

---

### Loading in Next.js!

We must build the loader manually in case of react and import and route it using lazy function, suspense, and fallback. But in the case of Next.js, we just make a file named as `loading.js/tsx/jsx` and it automatically shows its functionality.

---

### **Data Fetching -** [**Caching Data**](https://nextjs.org/docs/app/building-your-application/data-fetching/fetching-caching-and-revalidating#caching-data)

Caching stores data so it doesn't need to be re-fetched from your data source on every request. `( Matlab cache memory ma store garera rakhxa, Exact yehi kam garna react ma Loader use garna parthiyo )`

```javascript
// 'force-cache' is the default, and can be omitted
fetch('https://...', { cache: 'force-cache' })
```

---

### Data Fetching - Server Side Rendering

([**Fetching Data on the Server**](https://nextjs.org/docs/app/building-your-application/data-fetching/patterns#fetching-data-on-the-server)**) Next docs says:**

<mark>Whenever possible, we recommend fetching data on the server. This allows you to:</mark>  
`In case of Server Side Rendering, everytime data is fetch and its value is not stored in the cache memory. Vaneko jatibela chahinxa tetibela nai fetch garne chai SSR ho`

* ### <mark>Advantages!!!</mark>
    
    * **Direct Backend Access:**
        
        * Interaction with databases and data resources.
            
    * **Enhanced Security:**
        
        * Protects sensitive information on the server.
            
    * **Server-Side Rendering (SSR):**
        
        * Reduces back-and-forth with the client.
            
        * Minimizes main thread work on the client.
            
    * **Batched Data Fetching:**
        
        * Retrieves multiple data sets in a single round-trip.
            
    * **Reduced Waterfalls:**
        
        * Mitigates client-server waterfalls.
            
    * **Optimized Latency:**
        
        * Fetching data closer to data sources.
            
    * **Server-Side Techniques:**
        
        * Utilizes server components, route handlers, and actions.
            
    * **Efficient Handling:**
        
        * Streamlines multiple data fetches on the server.
            
    * **Improved Responsiveness:**
        
        * Enhances application responsiveness.
            
    
    Adopting server-side data fetching enhances efficiency, security, and performance, particularly in handling sensitive information and optimizing data retrieval.
    

---

### Default - Static Site Generation:

<mark>By Default Next.js fetches data using Static site Generation!</mark>

Static Site Generation ma Yo {`cache: ' no-store'}` hunna!

`Yo method ma data fetch garera matra cache ma store pain garxa! Jasko value frequently change hudaina tesko lagi yo method chai thik ho. Ek choti fetch garxa ani data store garxa!!!`

```javascript
 const res = await fetch(`https://api.example.com/posts/${params.id}`);
```

---

### Data Fetching - Incremental Static Generation.

`yo chai hybrid approach ho, jaha Static Site generate garne bela ma time every 3600 sec ma feri data fetch garera cache ma store garxa!`

Combination of Both Method!

```javascript
fetch('https://...', { next: { revalidate: 3600 } })
```

---

### API-endpoints for the backend!

In `app/api/users` this will lead us to `http://localhost/api/users`

```javascript
export async function GET(request: Request) {
    // write backend logic here
    return new Response('Hello world from User route! Get Methods');
}
```

A similar case happens in the GET, POST, PUT ... methods also.

> "Happy Face, Happy Reader" - Feel free to ask anythings even my income too! I am just a text away!!!🫶🚀