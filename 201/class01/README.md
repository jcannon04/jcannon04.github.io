# Getting Started

This sections reading is about getting started with everything you need to begin your web development journey. It is important to read or skim the all the material, but do not get stuck on one topic for too long. The idea is not to memorize everything you see. There will be plenty of time for that in the future. For now just read and try to get a elementary understanding for the basics and a feel for what we will be deep diving in to later. This introduction is very important for this introductory module because you get a chance to preview what we will be learning.

## Reading Q&A

1. Compose a short poem describing how HTTP 
sends data between computers.

    HTTP is exactly what it needs to be 
    computer talk can be such a bore
    clients talks to servers
    and nothing more
    packets come and go
    some fast some slow
    if their 404 they can't be found
    but if their 200 you're good to go
    these https are all about status
    they've got some big headers

2. Describe how HTML, CSS, and JS files are “parsed” in the browser.

    After a client's computer sends a request to a server and the server responds with a 200OK msg, the files for the website are sent in chunks called packets. The browser on the client machine reads the HTML code first. When it comes across CSS `<link>`s or javascript `<script>`s it sends more requests to the server to retrieve those files. It build a tree like object representing the html element and structure of the page call the DOM. It also builds a model of the CSS called CSSOM and compiles and executes all the javascript. Whiling doing all this work behind the scenes your browser also paints a visual representation of these file to the client's screen.

3. How can you find images to add to a Website?

    Google images is a great place to start. You can visit google and search for just about any image you can think of. Just be care not to include copyrighted images. Luckily, good provides a tool to filter out copy right images from the search

4. How do you create a String vs a Number in JavaScript?

    a string is wrapped in either`'single quotes'` or `"double quotes" and number is represented by a combination of numbers and dots and other math symbols like - and +

5. What is a Variable and why are they important in JavaScript?

    Variables are a mechanism for naming and storing data for later use. The are a common feature of most if not all programming languages. They are important to javascript for the same reason they are important in all programming languages. They allow you to store data and reference it by name later in your code. They are used for readability and and efficiency. I couldn't image programming without them. You would have to write out or copy and paste all the actually data every time! Yikes!

6. What is an HTML attribute?

    A HTML is part of an HTML element that defines a certain feature of the element and is not included in the content. You can use them to define the url of an image to be displayed in an img tag or the file to be added to your html via a script element

7. Describe the Anatomy of an HTMl element.

    An html element includes an opening and possibly a closing tag. The attribute and their associated value and the content to be displayed in your element on the page

8. What is the Difference between <article> and <section> element tags?
    An article defines a part of a webpage that could stand on it's own like a blog post or magazine article. The section tag is used to break up a page or part of a page into logical sections and subsections like contact info or details. An article can be made of multiple sections and a section could be made up of multiple articles. It depends on the layout requirements of a particular design.

9. What Elements does a “typical” website include?
    Most typical websites would include a  header: `<header>`, navigation bar `<nav>`, main content section`<main>` with possible `<article>`s and `<section>`s or `<div>`s, possibly an `<aside>` and a `<footer>`.
    
10. How does metadata influence Search Engine Optimization?
    Specifying a **description** in your meta data and having keywords that are related to what your site is about is important for SEO. Doing this will allow your site to appear high in the rankings in searches relevant to your site.

11. How is the <meta> HTML tag used when specifying metadata?
    Meta elements are the official way of adding meta data to your website. With a meta tag you can specify the main language of your site, the character set you want to use, a description, an author, and more.

12. What is the first step to designing a Website?
    You need to know your goals and visions for your website. What do you want to accomplish with your site? Essentially you need to brainstorm about why your building a website and what you want from it before you get caught up in the technicalities.

13. What is the most important question to answer when designing a Website?
    What exactly do I want to accomplish? (according to the this (article)[https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Design_and_accessibility/Thinking_before_coding])

14. Why should you use an <h1> element over a <span> element to display a top level heading?
    The `<h1>` tag is semantic it tells you and the browser that you are defining a heading. The span tag is ambiguous and doesn't tell you much of anything about what you are trying to accomplish with the format of your content.

15. What are the benefits of using semantic tags in our HTML?
    They tell developers and the browser information about how you elements fit into the format of your page and the meaning of the content between your tags. The are also helpful with accessibility and SEO.
16. Describe 2 things that require JavaScript in the Browser?
    Submitting user input to your server. Prompting user for info.

17. How can you add JavaScript to an HTML document?
    Linking a javascript file with a script tag. Writing code directly between script tags.