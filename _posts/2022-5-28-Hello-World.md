---
layout: post
title: Blog Post 2
published: true
---
# Creating a Text Utility app by using React and Hooks 
<figure>
<p align="center"> <img width="430" alt="www.google.com" height="450" src="https://i.imgur.com/BOQ0OAG.png"> 
<figcaption align="center"> Figure 1</figcaption> </p> 
</figure>



## Disclaimer

This blog is a continuation of the previous blog post ( Working with ReactJS and its functional components), in the previous blog, I covered what is ReactJS, functional components, and a small demo on that. In this blog, I will implement the basic understanding from the previous blog by working on creating a more functional Text Utility App. 

## Why Text Utility App

Before diving into this, you might be wondering why am I creating this Text Utility Application? What is the need for that and is it worth the time and hassle? So the answer to the above question is yes, it is worth it, and in this blog, we will see how you can create your own Text Utility Application and also how can you add features regarding Text such as copying the text, changing it to upper case/lower case and etc. The other reason for choosing this application is that by building this application I can use react Hooks to build almost everything in this application. The same functionality if done in HTML may take more time and more lines of code and it will be harder to implement logic in HTML. 

## About This Blog

As the name of the blog suggests what we will be working on in this blog and now without wasting any time let’s work on our Text Utility application which we created and enhance its functionality by just using ReactJS and demonstrate how powerful this JavaScript library is.

Before you jump into the practical part of this blog, make sure you have Text Utility Application framework ready from our previous blog so we can straight away continue. I will try my best to keep most of the demonstration in the video attached to this blog and focus theoretical part in the blog for the readers to learn and understand the basics. I hope you will enjoy reading this blog and learn a lot from the theory provided and my video demonstration. 

## A Quick Refresher

<figure>
<p align="center"> <a href="https://www.uxpin.com/studio/blog/react-native-vs-reactjs/">   <img width="360" alt="www.google.com" height="180" src="https://i.imgur.com/3jtBnIC.png"> </a>
<figcaption align="center"> Figure 1</figcaption> </p> 
</figure>

ReactJS is an open-source front-end JavaScript library to build interactive UIs. It is a very efficient, responsive, and fast JavaScript library available to build user interfaces. React uses JavaScript and HTML languages to build components and pages. With the help of ReactJS, components are made so easy to work with. It is expected that you know basic JavaScript, if not it is suggested to learn some basic JavaScript before moving forward. 

Functional components are those components that use concepts like props, hooks, and other various methods to enhance functionality. 

Props allow reusing components by enabling the feature of sending arguments to React components for creating unique components out of one component. 

Hooks in react were recently introduced (in 2018), and the main functionality of hooks is the freedom they provide by allowing the implementation of useState, useEffect, and many other ReactJS features without having to create a separate class for those features and states.

In the previous blog, I explained the concept of React and hooks in ReactJS. Additionally, I made a basic webpage of Text Utility App and how we can add a text to the textbox and set the text in uppercase, all with the help of hooks. 


## Adding More logic to Text Utility App

Currently, this app only converts text to upper case, which may not be very helpful. To make this application better and enhance its functionality, I will explain how to add more functions to this application. In this topic, I will be explaining how to implement those functions and how you can add your own custom features, in case you work with writing text a lot. To help you understand this better, I will be adding and explaining a couple of functionalities, after understanding you can add more features that you like easily.  For now, this app only converts text to upper case so I will add another button that does the opposite of that by changing the text to lowercase. The idea here is the same which is changing the state of the object to lowercase using useState. Remember how I made the function handleUpper in the previous blog which gets triggered when the button “Convert to Uppercase” is clicked in the textform.js file. I am doing the same thing here but for converting to lower case this time, so I am adding another button and calling it “Convert to Lowercase” and on clicking, this button will trigger another function called handleLower which converts all the text entered in the text box to lower case. Below is the code of the function handleLower and the button:


<p align="center">  <img width="450" alt="www.google.com" height="120" src="https://i.imgur.com/SFkBMZU.png"> </p> 

<p align="center"> <img width="900" alt="www.google.com" height="20" src="https://i.imgur.com/IaxpPb3.png">  </p> 

Secondly, I am adding another functionality that will allow a user to copy all the text inside the text box again by using react hooks concept. The idea is the same but only the code inside the function changes. In this case, we are declaring a variable text and using “getElementById” and passing the value of the id of the text field which in my case is “exampleFormControlTextarea1”. Change this value to the ID you have set for the text field. This function then uses the navigator function that writes the text to the clipboard, hence resulting in copying the text. Below is the code for that function:

<p align="center">  <img width="450" alt="www.google.com" height="120" src="https://i.imgur.com/KFmqlsM.png"> </p> 

<p align="center"> <img width="900" alt="www.google.com" height="20" src="https://i.imgur.com/BP91qtN.png">  </p> 




## What's new in React v18.0?


The latest version of react is **React v18.0**, let’s quickly dive into some of the new features and upgrades react has to offer in this version, and how it’s better than previous ones. To check the react version, simply go to the package.json file and all the components versions are listed there. The new upgrade comes with features like _automatic batching and startTransition API_. The most important mechanism introduced in React 18 is **concurrency**. It enables react to create multiple versions of any react page. Concurrency in react is a complex topic to study for now but will be very helpful to work with during later stages of our learning react. 
In addition to that, **Suspense** is also introduced, which eases data accessing in react applications. Suspense allows the user to specify the loading state for a part that is not ready to be displayed yet. Coming to the features, let’s start with **Transitions**. Suspense and transitions work well together. Transitions are used to differentiate between urgent and non-urgent updates. The term urgent updates here refer to direct user interactions like typing, clicking, etc. whereas non-urgent refers to moving from one user interface to another like an indirect interaction. Adding an import statement “ import {startTransition} from ‘react’; “ enables react to know which updates are urgent. [1]

## Creating our first React App with Bootstrap

Before starting with functional components, let’s make a simple react page.
But before that, I want to share a tool with my readers here, what if I tell you that there exists a tool that provides you with code for most of the components developers use in creating a website. Well, you might have guessed I am talking about **Bootstrap** here. For those who don’t know about bootstrap, bootstrap is a platform where users can find CSS, HTML, and JavaScript components and templates. For react, we will also be using Bootstrap so we can focus more on react rather than spending time on HTML and CSS. Now let’s get started, we will make an app with the help of bootstrap. 
Open the react app you have created at the beginning of the blog. Go to the App.Js file, and clear out all the code inside the return statement. Now we will be writing our code inside the return statement. Now, before using bootstrap code in our react app we have to add bootstrap script files in index.html.
 From bootstrap, locate the starter template provided and copy the Bootstrap JavaScript and CSS scripts and paste it into the Index.html file under the public folder. Copy any bootstrap code of various components and paste it into App.js and save. Now you might be getting a few errors in the App.js. Nothing to worry about here this is because the components we copied from bootstrap are not in JSX but in HTML. To make it work, we will be doing some changes here, change all the **“class=” to “className=”**. And add **“/”** at the end of the input tags, and any other tag if it does not have an ending tag. Explore bootstrap components and create your personalized react-app.

Hurray! another milestone achieved, now you can create a basic react app with the help of bootstrap.


## What are the functional components?

Now is the right time to introduce some functional components in react. **Functional components** are those components that use concepts like props, hooks, and other various methods to enhance functionality. This might sound confusing at first but hold on we will start from props and go all the way to hooks and their implementations.

### Understanding Props and PropTypes

Starting with the props, they make coding easier by not making us write overhead code. To write less code and get more output is something everyone wants. To make this true, react introduced props. **Props** allow reusing components by enabling the feature of sending arguments to React components for creating unique components out of one component. With the help of props, developers can reduce the number of pages or components in the react app and get the most out of one single component. To understand this better, here is an example below:

Inside of App.js, let’s assume you are calling a component Greet and to pass argument you will be using props like this:

<Greet name=”Saksham” message=”Have a good day” />;

Now, the function Greet will take the argument props from the calling program and it will look like this:

Export default function Greet(props) {  
return <p> Hello {props.name} ! {props.message}</p>

}

The output will be:  Hello Saksham ! Have a good day

As you can see in the example above the props.name is **JavaScript**, therefore it is written inside curly braces in the function. Now, with that example, you can pass different name values and the component Greet will display accordingly. You can also pass an object using props.

You can also create a **propType**, to ensure the argument passed should be a particular datatype like string etc., for example in the above example, propType will look like this:

import PropTypes from ‘pro-types’;

Greet.propTypes = {

name: PropTypes.string

}

It would give an error on the console if the argument passed is not a string.

You can also set default values with props using

Greet.defaultProps = {

name: ‘user’

}

This will set the default value of name as user.

### Understanding Hooks

**Hooks** in react were recently introduced (in 2018), and the main functionality of hooks is the freedom they provide by allowing the implementation of _useState, useEffect_, and many other ReactJS features without having to create a separate class for those features and states.

These components when implemented enhance the functionality and usability of the functional components. Hooks can only be called and used in functional components. Hooks make it easier and faster to code with efficiency by not making users write more overhead code, therefore resulting in making the code look cleaner.

Below is an example of useState,
<p align="center"> <img width="550" alt="www.google.com" height="30" src="https://i.imgur.com/As0Zp5D.png"> </p>

In the above example, the variable text is created and its default value is set as “Enter text here”, if you want to change its value , the setText variable is called. My video demonstration of this explains this more clearly and better.

In the past when hooks were not introduced, class-based components can only be used to store and manage the state of the objects, but today hooks made it possible to store and manage the state of the objects without having to create a class in a functional component. Overall, it is quite interesting to learn hooks and how they work in web applications. [1]

## Video 

<div class="embed-responsive embed-responsive-16by9">

<iframe width="560" height="315" src="https://www.youtube.com/embed/BsZYHd8ndwU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

</div>


## References
**[1]** “React – a JavaScript library for building user interfaces,” _– A JavaScript library for building user interfaces_. [Online]. Available: https://reactjs.org/. [Accessed: 14-Jun-2022]. 

**Figure 1** “React native vs. reactjs - understand the difference,” _Studio by UXPin_, 18-Feb-2022. [Online]. Available: https://www.uxpin.com/studio/blog/react-native-vs-reactjs/. [Accessed: 14-Jun-2022].
