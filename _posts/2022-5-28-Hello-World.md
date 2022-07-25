---
layout: post
title: Blog Post
published: true
---
# Creating a Text Utility app by using React and Hooks 
In the presence of HTML, and CSS-like front-end libraries that get the work done, why would we need to learn React? Well, let’s figure out the answer to this together by learning React and what makes it better than HTML and why is this used more nowadays. 
<figure>
<p align="center"> <a href="https://www.uxpin.com/studio/blog/react-native-vs-reactjs/">   <img width="360" alt="www.google.com" height="180" src="https://i.imgur.com/3jtBnIC.png"> </a>
<figcaption align="center"> Figure 1</figcaption> </p> 
</figure>


## What is ReactJS?

Let’s start by introducing ReactJS, **ReactJS** is an open-source front-end JavaScript library to build interactive UIs. It is a very efficient, responsive, and fast JavaScript library available to build user interfaces. React uses **JavaScript** and **HTML** languages to build components and pages. With the help of reactJS, components are made so easy to work with. 
_It is expected that you know basic JavaScript, if not it is suggested to learn some basic JavaScript before moving forward._

## Understanding JSX and its purpose

**JSX** is an extension of JavaScript syntax.[1] JSX is not required but it is preferred to use in React. The main feature of JSX is that it allows you to write JavaScript inside JSX using curly braces. In simple words, JSX is like a combination of HTML, JavaScript, and CSS. JSX may not look very different from HTML but yet there are some differences between the two. 
_To learn more about JSX, feel free to check online resources._
 If you know HTML, JSX will not be a problem in React.
 **A common question about what is the need for JSX in react?**
 So the answer is that JSX allows you to write JavaScript, HTML, and CSS together, therefore you can do JavaScript logic with HTML, and CSS components. Hence, bringing all three together in one place to provide a better developer experience. If you are using JSX in react then you can only return one element. If you want to return multiple elements, then either wrap all those elements inside the div tag or return elements as an array.

## Creating a framework for ReactJS

A quick hands-on for bringing life to react app, create a folder on your computer where you want to store all the react pages. In the next step, it is preferred to use Visual Studio, open a new terminal window in Visual Studio and type the command **“npx create-react-app &nbsp;name-of-the-react-folder”** and press enter.

Here in the example below, you can see that a react app named my-react is created.

<p align="center">  <img width="450" alt="www.google.com" height="30" src="https://i.imgur.com/2b3Ukp3.png">  </p> 

After executing this command, it will load all the necessary files and folders inside the folder created in the first step, these files and folders are used to run react app, and they can be modified according to our needs.

To run a react app, simply type “npm start” in the terminal, and then it will run the react app on the default browser. Make sure you are in the right folder before doing “npm start” or else you will get errors. To move to the right folder use the “cd name of folder” command in the terminal. 
_Hurray! You have successfully created your first frame of react app._
Whenever you will be working on a react app. These steps remain the same.

## Understanding the default files and folders


Out of all the files installed through installation, the **src** folder contains an App.js file, which is the main file containing all the components used in the react app and the logic behind that.  The src folder contains a file index.js, index.js is like a starting point in react app. If you read the code inside of index.js, it states to run the App component where id is root. This is the reason why App.js runs when the **“npm start”** command is issued in the terminal.

<p align="left">  <img width="250" alt="www.google.com" height="200" src="https://i.imgur.com/Nk4S3kN.png">  &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
  <img width="280" alt="www.google.com" height="140" src="https://i.imgur.com/frGbISc.png">  </p> 

Inside App.js, the code written is the JSX. It is preferred that App.js should not contain any JSX code, instead should be used in components, and components should be rendered in the App.js file. By default, there is no component folder created by react. The developer has to create a components folder under the src folder where all the components will be stored like navbar.js, form.js, etc. Components can be reused, and they can be called from any page. Components can be made unique by-passing props to them, which we will be covering ahead.

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
