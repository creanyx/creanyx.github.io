---
layout: post
title: "Adding Bootstrap to Laravel"
Date: 11-11-2015
Author: Ahmed Khakwani 
---
Laravel is a free, open source PHP framework. Laravel was created by Taylor Otwell. It is intended for web application which are following the MVC architectural pattern. As of March 2015 Laravel is regarded as one of the most popular PHP framework. 

Now bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web. Many web developers use bootstrap for designing UI. Now bootstrap has html formatting rules, if you follow those rules then your site will adjust it’s UI according to screen width, and by following those HTML formatting rule
<img> https://raw.githubusercontent.com/Sakina-Murtaza/image/607765171a1a9b81afbb63ca97f86714903d0b87/bootstrap-code1.png </img>
JavaScript will work on HTML. Like in bootstrap 3 for fixed navbar, html formatting should be like that 
Using Bootstrap in Laravel projects is not that difficult. Like other CSS and JS files, just place “bootstrap.css” or “bootstrap.min.css” in “laravel_installation_path/public/assets/css”, and place “bootstrap.js” or “bootstrap.min.js” in “laravel_installation_path/public/assets/js”. Now anywhere in you view files write that line 
<pre><code> asset('assets/css/bootstrap.css')</code></pre>
* or if you are using bootstrap minified CSS then write
<pre><code> asset('assets/css/bootstrap.min.css')</code></pre>
* and for js files please write that line anywhere in your view files
<pre><code> asset('assets/js/bootstrap.css')</code></pre>
* or if you are using bootstrap minified JS then write
<pre><code> asset('assets/js/bootstrap.min.js')</code><pre>
Now, bootstrap also comes with “glyphicons”. Bootstrap use “glyphicons” for different symbols and these symbols increases site usability. Just copy “glyphicons” files to “laravel_installation_path/public/assets/fonts”. By following these steps bootstrap will be able to fetch font files. 