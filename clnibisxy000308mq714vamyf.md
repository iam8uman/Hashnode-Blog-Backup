---
title: "How to Dynamically Change Background Colors in React Using State || Tailwindcss"
seoTitle: "How to Dynamically Change Background Colors in React Using State ||"
seoDescription: "How to Dynamically Change Background Colors in React Using State || Tailwindcss
Let's Make Colors Dance in React!"
datePublished: Mon Oct 09 2023 03:13:04 GMT+0000 (Coordinated Universal Time)
cuid: clnibisxy000308mq714vamyf
slug: how-to-dynamically-change-background-colors-in-react-using-state-tailwindcss
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696821100325/7e313757-3bf0-455e-b571-32871e4a1771.png
tags: reactjs, background-color, tailwind-css, bgchange, whysumancode

---

---

Hey there, my little explorer! Today, we're going to learn something super cool in the world of coding. We're going to make colors dance on the screen in our React app. 🌈

## What's React, You Ask?

Well, think of React like your magic coloring book. It helps us create amazing pictures on the computer screen. But instead of crayons, we use special words and instructions.

## Setting Up Our Playground

Before we start coloring, let's set up our playground. We'll need some buttons to choose colors and a big area to see our masterpiece. Think of it like your coloring book and a box of crayons.

```jsx
import { useState } from "react";

function App() {
  // Our magic color box!
  const [color, setColor] = useState("red");

  // Our color-changing wand!
  const bgChange = (newColor) => {
    setColor(newColor);
  };

  return (
    <>
      {/* This is our coloring book page */}
      <div className={`mainbody bg-${color}-700 h-screen w-screen`}>
        {/* These are our crayons */}
        <div className="btnList flex flex-wrap inset-x-10 fixed bottom-10 gap-10 justify-center bg-slate-400 p-5 rounded-lg">
          <button className="bg-red-700" onClick={() => bgChange("red")}>
            Red
          </button>
          <button className="bg-purple-700" onClick={() => bgChange("purple")}>
            Purple
          </button>
          <button className="bg-green-700" onClick={() => bgChange("green")}>
            Green
          </button>
          <button className="bg-yellow-700" onClick={() => bgChange("yellow")}>
            Yellow
          </button>
        </div>
      </div>
    </>
  );
}

export default App;
```

## The Magic Behind the Curtain

Okay, let me explain the magic part:

* `useState` is like our magic color box. It helps us keep track of the current color.
    
* `bgChange` is like a magic spell. When we press a button, it tells our color box to change to a new color.
    

## Painting with Buttons

Now comes the fun part! Each button is like a magical crayon that changes the color. When we click a button, our coloring book's background magically changes to that color.

So, if we click the "Red" button, our coloring book becomes red. Click "Purple," and it turns purple. You get the idea!

## Time to Play!

You can try this at home too, using your coloring book and crayons. But here, we're doing it on the computer!

Isn't it amazing? You're like a little wizard making colors dance on the screen. Have fun, my little artist! 🎨✨

---

And that's it! We've learned how to make colors dance on the screen in our React app using some magic spells (code) and our colorful crayons (buttons). Keep exploring, and remember, coding is like painting with words! 🌟