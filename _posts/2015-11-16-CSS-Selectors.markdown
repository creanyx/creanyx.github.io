---
Layout: post
Title: "CSS Selectors"
Author: Ahmed Khakwani
---
*CSS selectors are basically CSS rules that selects the HTML elements you want to style. After selecting you can apply any type of styles like text-color and background on those HTML elements. Let us look at different CSS selectors available.</p>

*To apply CSS style on all HTML elements you need to write

<code>
* { 
color: green;
font-size: 20px;
line-height: 25px;
}
</code>

*That style will be applied on all HTML elements in a page. To apply CSS style on all elements with same tag name you need to write 


<code>
p {
color: green;
font-size: 20px;
line-height: 25px;
}
</code>

Here "P" is tag name 

In that code "P" is tag name, it can be any other tag name. Using that type of CSS selection you can apply CSS style on all DIV tags, Table tags, or any other HTML tag.
<h1> Now, how to Select HTML element using its attribute name </h1> Mostly we used to select "Input" tags with their attribute name. 

<code>
input[type='text'] {
   	color: green;
font-size: 20px;
line-height: 25px;
}
</code>

In that code we are selecting input tags which have attribute named "text" and attribute value is "text". To select input tags with type submit we need to write


<code>
input[type='submit'] { 
color: green;
font-size: 20px;
line-height: 25px;
}
</code>

<h1> ID and Class Selectors </h1>

What are ID's and Classes. ID is HTML tag attribute, its like identity of HTML tag in whole page and main thing is it should be unique. Class is an HTML tag attribute, and more then one tag class can be same. Example of ID is like 

<code>
<div id="container"></div>
</code>

An example of class is like 

<code>
<div class="box"></div>
</code>

To assign CSS style to class "box" 

<code>
.box {
   	padding: 20px;
 	margin: 10px;
	width: 240px;
	}
</code>

and To assign CSS style to id "container" 
<code> 
#container {
   	padding: 20px;
   	margin: 10px;
   	width: 240px;
	}
</code>
If you want to apply CSS to a class or tag or id inside a class or id, then CSS gives you a solution for that. Consider HTML is like 
<code>
#container .box-2 {
	color: #000;
	font-size: 10px;
	background: url(any-image.png);
	}
</code>
<h1> Adjacent Siblings Combinator </h1>
A selector that uses the adjacent sibling combinator uses the plus symbol (+), and is almost the same as the general sibling selector. The difference is that the targeted element must be an immediate sibling, not just a general sibling. For that  CSS code should be like: 

<code>
p + p {
   font-size: 1.5em;
   margin-bottom: 0px;
}
</code>

<h1> Apply CSS effects on mouse hover, active, focus and visited </h1>

Too apply CSS effect on mouse hover CSS should be like 

<code> 
a:hover {
	color: red;
	}
	</code>
For active CSS should be like
<code> a:active {
	color: red;
	}
</code>
For visited CSS should be like 
<code>
a:visited {
	color: red;
	}
</code>
For focus CSS should be like
<code>
a:focus {
	color: red;
	}
</code>
Now the question I have in mind, can we use these CSS selectors in jQuery? 















