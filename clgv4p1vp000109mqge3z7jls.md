---
title: "That's How Stephen Hawking Communicate, Text To Speech In 3 Lines Of JavaScript."
seoTitle: "That's How Stephen Hawking Communicate, Text To Speech In 3 Lines Js"
seoDescription: "That's How Stephen Hawking Communicate, Text To Speech In 3 Lines Of JavaScript."
datePublished: Mon Apr 24 2023 17:45:02 GMT+0000 (Coordinated Universal Time)
cuid: clgv4p1vp000109mqge3z7jls
slug: thats-how-stephen-hawking-communicate-text-to-speech-in-3-lines-of-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682358205329/1cf33933-2c2f-4022-993a-19adb98ddadf.png
tags: js, reactjs, html5, sumannn, me8848you

---

### If you just want only code then, it is given below:

```javascript
var msg = new SpeechSynthesisUtterance();
msg.text = "Happy Face,Happy Reader";
window.speechSynthesis.speak(msg);
```

### If you want a complete explanation also then you have to read this article entirely.

\--&gt;Don't be afraid it is quite simple as a function in JavaScript. If you're not in a rush, this article provides a comprehensive guide on utilizing JavaScript to transform the text into speech, also known as spoken words, on the web.

\*\*To Start this, First we must find out that your browser support Speech synthesis API or Not for this :

```javascript
if ('speechSynthesis' in window) {
 alert("Broswer supports speech synthesis 🎉");
// Support the write code 
}else{
  alert("Sorry, your browser doesn't support the speech synthesis API !");
//very soon available in this browser
}
```

### Next step is to create a new speechSynthesis object,

```javascript
var msg = new SpeechSynthesisUtterance();
msg.text = "Happy Face, Happy Reader";
window.speechSynthesis.speak(msg);
```

### Code Explanation

* Line 1: We created a variable `msg`, and the value assigned to it is a new instance of the `speechSynthesis` class.
    
* Line 2: The `.text` property is used to specify the text we want to convert to speech
    
* And finally, the code on the 3rd(last) line is what actually makes our browser talk.
    

## Whole Code

```javascript

  // **************************************************

  // text to speech

  function speak(){

    // Check if the browser supports the speech synthesis API
    if ("speechSynthesis" in window) {
      // Create a new instance of the SpeechSynthesisUtterance object
      const message = new SpeechSynthesisUtterance();

      // Set the text that you want to convert to speech
      message.text = "Hello, how are you today?";

      // Choose the voice that you want to use (optional)
      // message.voice = speechSynthesis.getVoices()[0];

      // Choose the speech rate (optional)
      // message.rate = 0.7;

      // Choose the pitch (optional)
      // message.pitch = 1.2;

      // Call the speech synthesis function to convert text to speech
      window.speechSynthesis.speak(message);
    } else {
      // If the browser doesn't support the speech synthesis API, show an error message
      console.log("Sorry, your browser doesn't support text to speech!");
    }
  };

  // **************************************************************
```