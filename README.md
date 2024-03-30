# JS-Data-Manipulation
Data Manipulation using JavaScript.  With common snippets &amp; so much more.

https://michaelsoriano.com/common-javascript-snippets-for-data-manipulation/

Advanced DOM Manipulation Techniques with JavaScript

In the world of web development, dynamic and interactive web pages are essential to engage users and provide a seamless browsing experience. JavaScript, as a powerful scripting language, plays a crucial role in manipulating the Document Object Model (DOM) to create, modify, and delete HTML elements dynamically.

In this article, we will explore advanced DOM manipulation techniques using JavaScript, enabling you to take your web development skills to the next level. We will cover practical examples and provide ample theory to help you understand the concepts thoroughly.

Understanding the DOM
Before diving into advanced techniques, let's briefly revisit the basics of the DOM. The DOM represents the structure of an HTML document as a tree-like structure, where each HTML element is a node. JavaScript allows us to interact with this tree-like structure, providing methods and properties to manipulate the nodes and their attributes.

Before we move ahead with the different advanced techniques of DOM manipulation, let's first explore the basic example on which we will make use of the different examples provided below.

Example

```
<!DOCTYPE html>
<html>
<head>
   <title>Advanced DOM Manipulation Techniques</title>
   <style>
      button {
        padding: 10px;
        margin-top: 10px;
      }
   </style>
</head>  
<body>
   <div id="container">
      <!-- Existing content -->
   </div>
   <button id="myButton">Click Me!</button>
   <p id="target">
      <a href="www.google.com"> Element </a>
   </p>
   <p id="paragraphToRemove">To Remove this paragraph.</p>
   <button id="removeButton">Remove Paragraph</button>
	
   <script>	
      // Creating and Appending Elements
      const container = document.getElementById("container");
      const newParagraph = document.createElement("p");
      newParagraph.textContent = "This is a dynamically created paragraph.";
      container.appendChild(newParagraph);
	  
      // Modifying Element Attributes
      const button = document.getElementById("myButton");
      button.addEventListener("click", function() {
        button.style.backgroundColor = "red";
      });
	  
      // paragraph to remove
      const removeButton = document.getElementById("removeButton");
      const paragraphToRemove = document.getElementById("paragraphToRemove");
      removeButton.addEventListener("click", function() {
        paragraphToRemove.remove();
      });
	  
      // customising link behaviour
      const link = document.querySelector("#target a");
      link.addEventListener("click", function(event) {
        event.preventDefault();
        alert("You clicked the link!");
      });
	  
      // traversing the DOM
      const targetElement = document.getElementById("target");
      const nextSibling = targetElement.nextSibling;
      if (nextSibling) {
        nextSibling.style.color = "blue";
      }	  
   </script>
</body>
</html>
```
Explanation
In this HTML page, we have a container with the ID "container" where we will append a dynamically created paragraph element. We also have a button with the ID "myButton" that changes its background colour when clicked. Additionally, there is a paragraph element with the ID "target" that we will traverse to find its next sibling and modify its text colour. Lastly, there is another button with the ID "removeButton" that removes a specific paragraph element when clicked.

Now before we move on the examples where we will explore the different DOM manipulation techniques, we need to make sure that we put all the code shown in the points below in the scripts.js file and then run the index.html file again.
