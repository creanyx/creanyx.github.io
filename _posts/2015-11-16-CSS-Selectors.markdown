---
layout: post
title: "CSS Selectors"
date: 2015-11-18
authorbio : Ahmed Khakwani
---

CSS selectors are basically CSS rules that selects the HTML elements you want to style. After selecting you can apply any type of styles like text-color and background on those HTML elements. Let us look at different CSS selectors available.
To apply CSS style on all HTML elements you need to write

``{ 
color: green;
font-size: 20px;
line-height: 25px;
}``

That style will be applied on all HTML elements in a page. To apply CSS style on all elements with same tag name you need to write 
`` p {
color: green;
font-size: 20px;
line-height: 25px;
}``

Here "P" is tag name 

In that code "P" is tag name, it can be any other tag name. Using that type of CSS selection you can apply CSS style on all DIV tags, Table tags, or any other HTML tag.

<h2> Now, how to Select HTML element using its attribute name </h2> 

Mostly we used to select "Input" tags with their attribute name.

 
``input[type='text'] {
   	color: green;
font-size: 20px;
line-height: 25px;
}``
In that code we are selecting input tags which have attribute named "text" and attribute value is "text". To select input tags with type submit we need to write

``input[type='submit'] { 
color: green;
font-size: 20px;
line-height: 25px;
}``

<h2> ID and Class Selectors </h2>

What are ID's and Classes. ID is HTML tag attribute, its like identity of HTML tag in whole page and main thing is it should be unique. Class is an HTML tag attribute, and more then one tag class can be same. Example of ID is like 

``<div id="container"></div> ``

An example of class is like 

``<div class="box"></div>``

To assign CSS style to class "box" 

``.box {
   	padding: 20px;
 	margin: 10px;
	width: 240px;
	}``
	
and To assign CSS style to id "container"
``#container {
   	padding: 20px;
   	margin: 10px;
   	width: 240px;
	}``
	
If you want to apply CSS to a class or tag or id inside a class or id, then CSS gives you a solution for that. Consider HTML is like 

``#container .box-2 {
	color: #000;
	font-size: 10px;
	background: url(any-image.png);
	}``
	
<h2> Adjacent Siblings Combinator </h2>
A selector that uses the adjacent sibling combinator uses the plus symbol (+), and is almost the same as the general sibling selector. The difference is that the targeted element must be an immediate sibling, not just a general sibling. For that  CSS code should be like: 

``p + p {
   font-size: 1.5em;
   margin-bottom: 0px;
   }``

<h2> Apply CSS effects on mouse hover, active, focus and visited </h2>

Too apply CSS effect on mouse hover CSS should be like 

``a:hover {
	color: red;
	}``
	
For active CSS should be like
``a:active {
	color: red;
	}``
	
For visited CSS should be like 
``a:visited {
	color: red;
	}``	

For focus CSS should be like
``a:focus {
	color: red;
	}``
	
Now the question I have in mind, can we use these CSS selectors in jQuery? 
