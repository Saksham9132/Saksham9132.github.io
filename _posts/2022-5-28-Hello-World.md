---
layout: post
title: Blog Post 2
published: true
---
# Creating a Text Utility app by using React and Hooks 

<p align="center"> <img width="430" alt="www.google.com" height="450" src="https://i.imgur.com/BOQ0OAG.png"> 
 </p> 

## Disclaimer 👀

This blog is a continuation of the previous blog post ( Working with ReactJS and its functional components), in the previous blog, I covered what is ReactJS, functional components, and a small demo on that. In this blog, I will implement the basic understanding from the previous blog by working on creating a more functional Text Utility App. 

## Why Text Utility App 🤔

Before diving into this, you might be wondering why am I creating this Text Utility Application? What is the need for that and is it worth the time and hassle? So the answer to the above question is yes, it is worth it, and in this blog, we will see how you can create your own Text Utility Application and also how can you add features regarding Text such as copying the text, changing it to upper case/lower case and etc. The other reason for choosing this application is that by building this application I can use react Hooks to build almost everything in this application. The same functionality if done in HTML may take more time and more lines of code and it will be harder to implement logic in HTML. 

## About This Blog 😎

As the name of the blog suggests what we will be working on in this blog and now without wasting any time let’s work on our Text Utility application which we created and enhance its functionality by just using ReactJS and demonstrate how powerful this JavaScript library is.

Before you jump into the practical part of this blog, make sure you have Text Utility Application framework ready from our previous blog so we can straight away continue. I will try my best to keep most of the demonstration in the video attached to this blog and focus theoretical part in the blog for the readers to learn and understand the basics. I hope you will enjoy reading this blog and learn a lot from the theory provided and my video demonstration. 

## A Quick Refresher 👍

<figure>
<p align="center"> <a href="https://www.uxpin.com/studio/blog/react-native-vs-reactjs/">   <img width="360" alt="www.google.com" height="180" src="https://i.imgur.com/3jtBnIC.png"> </a>
<figcaption align="center"> Figure 1</figcaption> </p> 
</figure>

ReactJS is an open-source front-end JavaScript library to build interactive UIs. It is a very efficient, responsive, and fast JavaScript library available to build user interfaces. React uses JavaScript and HTML languages to build components and pages. With the help of ReactJS, components are made so easy to work with. It is expected that you know basic JavaScript, if not it is suggested to learn some basic JavaScript before moving forward. 

Functional components are those components that use concepts like props, hooks, and other various methods to enhance functionality. 

Props allow reusing components by enabling the feature of sending arguments to React components for creating unique components out of one component. 

Hooks in react were recently introduced (in 2018), and the main functionality of hooks is the freedom they provide by allowing the implementation of useState, useEffect, and many other ReactJS features without having to create a separate class for those features and states.

In the previous blog, I explained the concept of React and hooks in ReactJS. Additionally, I made a basic webpage of Text Utility App and how we can add a text to the textbox and set the text in uppercase, all with the help of hooks. 


## Adding More logic to Text Utility App 🔥

Currently, this app only converts text to upper case, which may not be very helpful. To make this application better and enhance its functionality, I will explain how to add more functions to this application. In this topic, I will be explaining how to implement those functions and how you can add your own custom features, in case you work with writing text a lot. To help you understand this better, I will be adding and explaining a couple of functionalities, after understanding you can add more features that you like easily.  For now, this app only converts text to upper case so I will add another button that does the opposite of that by changing the text to lowercase. The idea here is the same which is changing the state of the object to lowercase using useState. Remember how I made the function handleUpper in the previous blog which gets triggered when the button “Convert to Uppercase” is clicked in the textform.js file. I am doing the same thing here but for converting to lower case this time, so I am adding another button and calling it “Convert to Lowercase” and on clicking, this button will trigger another function called handleLower which converts all the text entered in the text box to lower case. Below is the code of the function handleLower and the button:


<p align="center">  <img width="450" alt="www.google.com" height="120" src="https://i.imgur.com/SFkBMZU.png"> </p> 

<p align="center"> <img width="900" alt="www.google.com" height="30" src="https://i.imgur.com/IaxpPb3.png">  </p> 

Secondly, I am adding another functionality that will allow a user to copy all the text inside the text box again by using react hooks concept. The idea is the same but only the code inside the function changes. In this case, we are declaring a variable text and using “getElementById” and passing the value of the id of the text field which in my case is “exampleFormControlTextarea1”. Change this value to the ID you have set for the text field. This function then uses the navigator function that writes the text to the clipboard, hence resulting in copying the text. Below is the code for that function:

<p align="center">  <img width="650" alt="www.google.com" height="120" src="https://i.imgur.com/KFmqlsM.png"> </p> 

<p align="center"> <img width="900" alt="www.google.com" height="30" src="https://i.imgur.com/BP91qtN.png">  </p> 

Lastly, I am adding another function that will clear all the text inside the text box using react hooks. This function just uses useState setText variable and set it to empty string, hence resulting in clearing all the text from the text field. The code for that functionality as as follows:

<p align="center">  <img width="350" alt="www.google.com" height="80" src="https://i.imgur.com/6ZHZ9Op.png"> </p> 

<p align="center"> <img width="900" alt="www.google.com" height="30" src="https://i.imgur.com/XA97dTX.png">  </p> 
In this way, we can create a useful text utility app, that can help us in our day-to-day life. By understanding these basic functions, you can create your personalized text utility app and add as many functions and features you want! 

To add more logic to functionality, this app will also count the number of words and characters typed into the text area. By using text.split(“ “).length , it will count the number of words in the text field, and for counting the character I used a simple function of text.length. 

<p align="center">  <img width="580" alt="www.google.com" height="100" src="https://i.imgur.com/Cw08yIW.png"> </p> 


## Changing themes on the App 🔄

Now let’s focus on making this application more user-friendly. You might have seen and used this feature in applications that allow the user to switch to dark or light mode.

<p align="center"> <a href="https://reinteractive.com/posts/403-simple-css-dark-theming-for-accessibility "> <img width="420" alt="www.google.com" height="360" src="https://i.imgur.com/3MZolFk.png"> </a> </p> 

Any app which offers the feature of personalization is gaining ground nowadays. People prefer to have the ability to switch themes or change to dark/light mode and have that personalized version of that app. In order to make our text utility app look cool, I will demonstrate how to implement this theme functionality on our text utility app by just using the basic react hook useState. In this part, we will be not only be using useState but also props to send values to different components and render them according to the mode selected. There is a switch in the navbar, which is a bootstrap component, it is the component with which our end user will switch modes. When dark mode is enabled, it will change the color of all the components in the app from text form color to all the text headings colors. Since, we are using useState to switch modes, therefore, there is no delay when switching between modes and it all happen smoothly. This is the reason I prefer to use react Hooks because of this advantage it offers. 

Below is the video demonstration of how you can implement changing dark mode, hope this makes it clear: 

<div class="embed-responsive embed-responsive-16by9">

<iframe width="560" height="315" src="https://www.youtube.com/embed/BO7qUbnf1lI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

</div>

## Wrapping Up 🙌

Yayy!🥳 You have reached to the end of this blog, now is the time to wrap it up with a quick summary, so this blog started with a quick refresher of Reactjs and hooks like useState and props that I have covered in the previous blog ( Working with ReactJS and its functional components). Then, I build and enhanced the Text Utility Application by introducing more logic and features to it. This application can be used as an text editor. I also explained how you can add custom features and different functionality according to your need. And therefore, can create a custom Text utility application. In order to make it look even better, I demonstrated how to add an option to change the mode from dark to light and vice versa. If you understood the concept, you can now make any react app and use hooks to add functions and features. Thanks for reading it, and I hope it was helpful. 😊  



## References
**[1]** “My Blog Post 1: Working with React and its functional components". 

**Figure 1** “React native vs. reactjs - understand the difference,” _Studio by UXPin_, 18-Feb-2022. [Online]. Available: https://www.uxpin.com/studio/blog/react-native-vs-reactjs/. [Accessed: 14-Jun-2022].
