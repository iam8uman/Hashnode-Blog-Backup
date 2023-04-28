---
title: "Dark Mode using React useState Hooks. No Backend Code."
seoTitle: "Dark Mode using React useState Hooks. No Backend Code."
seoDescription: "Dark Mode using React useState Hooks. No Backend Code."
datePublished: Fri Apr 28 2023 15:56:11 GMT+0000 (Coordinated Universal Time)
cuid: clh0qkh9n000d09lfhxajdpml
slug: dark-mode-using-react-usestate-hooks-no-backend-code
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682697230056/291a8408-4b64-4691-94d4-9d29a0566393.png
tags: reactjs, hooks, dark-mode, sumannn, me8848you

---

### Now, Here we go straight forward to the main topic:

* First of all, we have to make use of the useState hook for the dark mode CSS style as :
    
    ```javascript
    //useState Hook for darkmode 
    const [container,setContainer]=useState({
        color:'white',
        backgroundColor:'black',
        
      });
    ```
    
* Secondly, we use another useState hook for the button text, which also has to change during the dark and light modes.
    
    ```javascript
     // usestate hook for text inside buttion
      const[buttontext,setButtontext]=useState('Enable LightMode');
    ```
    
* Thirdly, we have now defined that state, then we have to change its CSS value when the button is clicked i.e. Enable/Disable Button.
    
    ```xml
    //Here,when button is clicked toggleLight function is invoked
    <button className="m-2 p-2 btn btn-light" onClick={toggleLight}>{buttontext}</button>
    ```
    
* Here when the button is clicked toggleLight function is invoked. Now we have to define the functionality for this button as :
    
    ```javascript
    const toggleLight=()=>{
    
        if(container.color==='white')
        {
          setContainer({
    
            color:'black',
            backgroundColor:'white',
          })
          setButtontext('Enable DarkMode')
        }
        else
        {
          // console.log(mode.color)
          // console.log("white")
          setContainer({
            color:'white',
            backgroundColor:'black',
          })
          setButtontext('Enable LightMode')
        }
      }
    ```
    
    That's it.
    

> "Happy Face, Happy Reader"-s2