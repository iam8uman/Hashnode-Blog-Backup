---
title: "LocalStorage || Store, Read & Clear ||"
seoTitle: "LocalStorage || Store, Read & Clear ||"
seoDescription: "LocalStorage || Store, Read & Clear ||
Day24 of #100daysofcode !"
datePublished: Wed Oct 18 2023 11:19:50 GMT+0000 (Coordinated Universal Time)
cuid: clnvnvgjy001909l9da7v3vtr
slug: localstorage
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697614398428/0d70465a-2e85-4a09-9b08-052da522169c.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1697627947733/59a414f6-6c2b-43a6-99b5-8d55c8eb192e.png
tags: localstorage, 100daysofcode, sessionstorage, whysumancode, browser-storage

---

`localStorage` is similar to [`sessionStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage), except that while `localStorage` <mark>data has no expiration time</mark>, `sessionStorage` data gets cleared when the page session ends — that Sure, here are the important points about `localStorage` and `sessionStorage` in JavaScript:

1. **localStorage and sessionStorage**:
    
    * Both `localStorage` and `sessionStorage` are web storage solutions in JavaScript that allow you to store **<mark>key-value pairs.</mark>**
        
2. **localStorage**:
    
    * Data stored in `localStorage` has <mark>no expiration time.</mark>
        
    * It persists across browser sessions and <mark>even after the browser is closed.</mark>
        
    * The data stored `localStorage` <mark>remains available until explicitly removed or until the user clears their browser cache.</mark>
        
3. **sessionStorage**:
    
    * Data stored `sessionStorage` is only <mark>available for the duration of the page session.</mark>
        
    * It gets cleared when the page session ends, typically when the <mark>user closes the page or the browser.</mark>
        
    * <mark>Data stored in </mark> `sessionStorage` is specific to the tab or window where it was created. <mark>It's not shared between tabs or windows.</mark>
        
4. **Private Browsing or Incognito Mode**:
    
    * In private browsing or incognito mode, the behavior of `localStorage` and `sessionStorage` may differ.
        
    * For `localStorage`, <mark>data in "private" tabs is cleared when the last "private" tab is closed.</mark>
        
    * For `sessionStorage`, <mark>data in "private" tabs is cleared when the tab itself is closed.</mark>
        
5. **Use Cases**:
    
    * `localStorage` is typically used for storing data that needs to persist across sessions, such as user preferences or cached data.
        
    * `sessionStorage` is used for data that should only be available during the current browsing session, like temporary state or data specific to a single page.
        
6. **Access**:
    
    * Both `localStorage` and `sessionStorage` can be accessed using JavaScript's `localStorage` and `sessionStorage` objects.
        

In summary, `localStorage` and `sessionStorage` are valuable tools for storing data in web applications, but choosing the right one is important based on the intended data lifespan and scope?

---

1. ### How to use local storage?
    

The following snippet accesses the current domain's local [`Storage`](https://developer.mozilla.org/en-US/docs/Web/API/Storage) object and adds a data item to it using [`Storage.setItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/setItem).

```javascript
localStorage.setItem("myCat", "Tom");
```

The syntax for reading `localstorage` items are as follows:

```javascript
const cat = localStorage.getItem("myCat");
```

The syntax for removing the `localStorage` item is as follows:

```javascript
localStorage.removeItem("myCat");
```

The syntax for removing all the `localStorage` items are as follows:

```javascript
localStorage.clear();
```

---

> ### REMEMBER\*
> 
> localstorage only stores string data in key-value pairs. So during storing data in localstorage we need to convert data into string. <mark>JSON-String</mark>
> 
> ```javascript
> JSON.stringfy(data)
> ```
> 
> And during reading from LocalStorage, we need to convert it <mark>String-JSON</mark>
> 
> ```javascript
> JSON.parse(localStorage.getItem("fname"));
> ```

---

> `"Every great developer you know got there by solving problems they were unqualified to solve until they actually did it." - Patrick McKenzie`