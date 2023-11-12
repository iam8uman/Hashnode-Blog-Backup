---
title: "Server Side Rendering | SSR? CSR? Next Feature- SEO, Routing, File-based routing, Fullstack"
seoTitle: "Server Side Rendering | SSR? CSR? Next Feature- SEO, Routing, File-bas"
seoDescription: "Server Side Rendering | SSR? CSR? Next Feature- SEO, Routing, File-based routing, Fullstack"
datePublished: Sun Nov 12 2023 18:34:03 GMT+0000 (Coordinated Universal Time)
cuid: clovte6fr000009ld67jl7vsy
slug: server-side-rendering-ssr-csr-next-feature-seo-routing-file-based-routing-fullstack
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699813815299/a4e93477-1a61-4893-8a22-ee28bc193f8e.png
tags: routing, seo, ssr, nextjs, csr

---

---

### Rendering?

Rendering converts the code you write into user interfaces.

---

### What is Client side & Server Side rendering and which one is better?

Client-side rendering (CSR) and server-side rendering (SSR) are two approaches to rendering web pages, each with its own advantages and disadvantages.

1. **Client-Side Rendering (CSR):**
    
    * In CSR, the rendering of the web page is primarily done on the client side, meaning in the <mark>user's browser.</mark>
        
    * The initial HTML content is minimal, and the <mark>browser downloads a JavaScript bundle that contains the code responsible for rendering and fetching additional data.</mark>
        
    * The JavaScript code then executes on the client's machine, dynamically creating and updating the DOM (Document Object Model) as needed.
        
    * ### `Simple vasa ma Client side rendering ma client le request gareko kura/page server ma request janxa. Server le tyo snga related HTML,CSS,JS client/browser lai send garxa. Ani client le tyo code lai translate garera page/components show garxa-->CSR.`
        
    
    **Advantages of CSR:**
    
    * Fast <mark>initial</mark> page load: Since only a minimal amount of HTML and CSS is initially sent to the client, the page can load quickly.
        
    * Good for highly interactive applications: CSR is well-suited for applications that require a lot of user interactivity and dynamic content updates.
        
    
    **Disadvantages of CSR:**
    
    * <mark>SEO challenges:</mark> Search engines may have difficulty indexing content that relies heavily on client-side rendering.
        
    * <mark>Slower perceived performance on slower devices: </mark> Initial rendering depends on the client's device and can be slower on less powerful machines.
        

---

1. **Server-Side Rendering (SSR):**
    
    * <mark>In SSR, the server sends fully rendered HTML pages to the client.</mark> The server performs most of the rendering before sending the content to the browser.
        
    * This can be achieved using frameworks like <mark>Next.js for React</mark> or Nuxt.js for Vue.js.
        
    * ### `Simple vasa ma Server-Side Rendering vaneko client le request gareko kura/page server ma request janxa. Server le tyo snga related HTML,CSS,JS client/browser lai send garnu ko satta server mai tyo code lai translate garera page/component nai client lai pathauxa --> SSR.`
        
        \---🫶---  
        `SSR le pre-rendered code yaniki already render vayeko page client lai send garxa jasle garda indexing and crawling ma help hunxa. So that SEO optimizes.`
        
        **Advantages of SSR**
        
    * <mark>Better SEO: </mark> Since the server sends fully rendered HTML to the client, search engines can easily index the content.
        
    * Improved initial load performance on slower devices: Users with slower devices experience faster initial page loads because they receive pre-rendered HTML.
        
    
    **Disadvantages of SSR:**
    
    * <mark>Longer initial page load time:</mark> The first request might take longer because the server needs to <mark>generate</mark> the HTML content before sending it to the client. `(Suru ma page load huna time lagxa)`
        
    * Increased server load: Server-side rendering can put more strain on the server compared to client-side rendering, especially in scenarios with a high number of requests. `(Server ma dherai request aairako hunxa, jhan Server side rendering le garda jhan load hunxa)`
        

**Which One is Better?** The choice between CSR and SSR depends on the specific requirements of your application:

* **Use CSR when:**
    
    * Your application is highly dynamic and relies heavily on client-side interactions.
        
    * You can address SEO concerns through other means, such as prerendering solutions.
        
* **Use SSR when:**
    
    * SEO is a critical factor for your application.
        
    * You want faster initial page loads, especially for users on slower devices.
        
    * The server load can be managed effectively.
        

In some cases, a hybrid approach called "Hybrid Rendering" or "Isomorphic Rendering" can be used, combining elements of both CSR and SSR to optimize performance and SEO. The choice depends on your specific use case, project requirements, and performance considerations.

---

### When to use React.js || Next.js?

REACT.JS -**CSR**\-&gt; When you need,

* <mark>highly dynamic and relies heavily on client-side interactions, better you use React.js,</mark>
    
* <mark>Also if SEO is not the main concern in your application.</mark>
    
* <mark>Also if you need a Faster initial load then you must use React.js</mark>
    
* In the case of Client-side rendering <mark>data fetching or managing user state</mark> is better.
    

NEXT.JS -**SSR**\-&gt; When you need,

* <mark>If SEO is the main issue then,</mark>
    
* <mark>You want faster initial page loads, especially for users on slower devices.</mark>
    
* <mark>Server le fully HTML web page nai render garxa that's why SEO enhance hune ho</mark>
    

---

### `NOTE*: Next.js provide flexibility that where to render your web pages i.e. Either in client or in Server. (J ma vayepani render garna milxa aafno requirement aanusar in Next) In next.js you can have SSR or CSR on your own choice.`

---

### File-based Routing System in Next.js

In the case of react.js, we use an additional package(third party) react-router-dom. But here in next.js, we used <mark>file-based routing.</mark>

---

### Next.js provides code splitting, what does it mean?

Code splitting is a technique, that breaks down the code in smaller chunks and load whenever they needed.

---

### Next.js also provides automatic loading when page is not available.

In react we have to use <mark>lazy()</mark> and also <mark>suspense</mark> and <mark>fallback</mark> like this. But in Next.js this functionality is automatic.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699718888303/b24767d8-d1ca-4e74-a377-7b2a348a4f6f.png align="center")

---

### Important\*\*\* : `Next js le hamlai dherai configuration ma time nalagau tyo mah automatic garidinxu, tmro main kam logic lekhne ho application ma tei gara vanxa!`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699719121832/0d03380b-db3b-4888-9615-146b0e94d497.png align="center")

---

### When to use CSR and SSR?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699810902460/2e24df12-7325-4ef2-b802-1e3d63fa8f51.png align="center")

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

> "Happy Face, Happy Reader" - Keep Going!