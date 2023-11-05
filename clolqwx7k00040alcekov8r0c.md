---
title: "NVM | Update & Upgrade Node and NPM version || Next JS, Creating Routes, Creating UI (Layout and Pages), Root Layout"
seoTitle: "NVM | Update & Upgrade Node and NPM version || Next JS, Creating Route"
seoDescription: "NVM | Update & Upgrade Node and NPM version || Next JS, Creating Routes, Creating UI (Layout and Pages), Root Layouts"
datePublished: Sun Nov 05 2023 17:26:57 GMT+0000 (Coordinated Universal Time)
cuid: clolqwx7k00040alcekov8r0c
slug: nvm-update-upgrade-node-and-npm-version-next-js-creating-routes-creating-ui-layout-and-pages-root-layout
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699205137330/1ffeb578-0d69-4d75-8204-48105cb93c68.png
tags: nextjs, nvm, whysumancode, update-npm-and-node, layouts-pages

---

---

1. ### NVM
    
    It is a node version manager, which is used to manage the node version. In simple language, if your device has the node 14 version and you want to use the node latest version for eg. 18. then you can use NVM like this.
    
    `Steps`
    
    1\. First install NVM from GitHub and search for it on Google & after installing NVM run its .exe file.
    
    2\. Check NVM Version using `nvm -v`
    

---

1. ### Install & upgrade node and npm versions
    
    After the successful installation of NVM, it is now its turn to upgrade node and npm. For this, you need to install the node version you want to download like this.
    

```javascript
nvm install 18.17.0
```

Now use this version, like this:

```javascript
nvm use 18.17.0
```

That's it. :)

---

1. ### Create Next app | I just finished React.js that's why I shifted to Next.
    
    For installation of the next app, I just searched <mark>Create next app</mark> then I found all the necessary requirements for installation of next app.
    
2. **<mark>WHY NEXT OVER REACT?</mark>**
    
3. Next.js: **The React Framework for the Web**
    
4. React Server Components
    
5. Nested Routes & Layouts
    
6. Simplified Data Fetching
    
7. Streaming & Suspense
    
8. Built-in SEO Support
    

---

### React Routing&gt; **Defining Routes**

This page will guide you through how to define and organize routes in your Next.js application.

## [**Creating Routes**](https://nextjs.org/docs/app/building-your-application/routing/defining-routes#creating-routes)

Next.js uses a file-system-based router where **folders** are used to define routes.

Each folder represents a [**route** segment](https://nextjs.org/docs/app/building-your-application/routing#route-segments) that maps to a **URL** segment. To create a [nested route](https://nextjs.org/docs/app/building-your-application/routing#nested-routes), you can nest folders inside each other.

![Route segments to path segments](https://nextjs.org/_next/image?url=%2Fdocs%2Fdark%2Froute-segments-to-path-segments.png&w=3840&q=75&dpl=dpl_9EKEbD7jAviauyTffgoEyAkQSGtP align="left")

A special [`page.js` file](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#pages) is used to make route segments publicly accessible.

![Defining Routes](https://nextjs.org/_next/image?url=%2Fdocs%2Fdark%2Fdefining-routes.png&w=3840&q=75&dpl=dpl_9EKEbD7jAviauyTffgoEyAkQSGtP align="left")

In this example, the `/dashboard/analytics` URL path is *not* publicly accessible because it does not have a corresponding `page.js` file. This folder could be used to store components, stylesheets, images, or other colocated files.

> **Good to know**: `.js`, `.jsx`, or `.tsx` file extensions can be used for special files.

---

## [**Creating UI**](https://nextjs.org/docs/app/building-your-application/routing/defining-routes#creating-ui)

[Special file conventions](https://nextjs.org/docs/app/building-your-application/routing#file-conventions) are used to create UI for each route segment. The most common are [`pages`](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#pages) <mark>to show UI unique to a route, and</mark> [`layouts`](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#layouts) <mark>to show UI that is shared across multiple routes.</mark>

---

# **Pages and Layouts**

## [**Pages**](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#pages)

A page is UI that is **<mark>unique</mark>** <mark>to a route</mark> (harek routing ma farak hune UI for eg. in about, contact, home etc..). We can define pages by exporting a component from a `page.js` file. Use nested folders to [define a route](https://nextjs.org/docs/app/building-your-application/routing/defining-routes) and a `page.js` file to make the route publicly accessible.

<mark>app/page.tsx</mark> --&gt; / URL

```typescript
// `app/page.tsx` is the UI for the `/` URL
export default function Page() { 
 return <h1>Hello, Home page!</h1>
}
```

Similarly,

<mark>app/dashboard/page.tsx</mark> --&gt; /dashboard URL

```typescript
// `app/dashboard/page.tsx` is the UI for the `/dashboard` URL
export default function Page() { 
 return <h1>Hello, Dashboard Page!</h1>
}
```

## [**Layouts**](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#layouts) **(reusable components)**

A layout is UI that is **<mark>shared</mark>** <mark>between multiple pages.</mark> On navigation, layouts preserve state, remain interactive, and do not re-render. Layouts can also be [nested](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#nesting-layouts).

### [**Root Layout (Required)**](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts#root-layout-required)

The root layout is defined at the top level of the `app` directory and applies to all routes. This layout enables you to modify the initial HTML returned from the server.

<mark>app/layout.tsx</mark>

```typescript
export default function RootLayout(
{  children}: {  children: React.ReactNode}
) {
  return (    
<html lang="en">      
    <body>{children}</body>    
</html>  
)}
```

\*IMPORTANT

> Root layout must have &lt;html&gt; and &lt;body&gt; tag coz Next does not create them. For SEO this tag are very important. In react there is only one tag &lt;div id="root"&gt; can't optimize the search engine that's why next is introduced"
> 
> ---