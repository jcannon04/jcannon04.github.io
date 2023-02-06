# Structure Web Pages With HTML

## What is HTML?

HTML stands for HyperText Markup Language. It is a markup language that tells the browser how to structure your web pages. HTML is made up of **elements** which you use to mark up your content and tell it how to appear or behave. HTML elements include tags that wrap your content to make links, emphasize text, and more. For Example Let's say we have some text:

```html
Hello World! This is my first line of HTML!
```
If we wanted to tell our browser that this text is a paragraph we could a `<p>` tag

```html
<p>Hello World! This is my first line of HTML!</p>
```
The browser would understand this code and display your paragraph on your screen like so:

<p>Hello World! This is my first line of HTML!</p>

## HTML Element Anatomy

An HTML element is made of up an opening tag, content, and a closing tag.

```html
<p>Hello World! This is my first line of HTML!</p>
```
* The first `<p>` is the opening tag. It marks where the element start and where the behavior of the element should start and take effect.
* In between the tags is the content of the element. In this example it is the paragraph's text.
* The final `</p>` include a forward slash to differentiate it from another opening tag. Marks the end of an element and it's effect

It's difficult with a `<p>` tag to see that the element has any effect on it's content. Let's take a look at the `<strong>` tag. This tag makes the text content bold:

```html
<strong>Hello world!</strong>
```
The browser would display (render) the following:

<strong>Hello world!</strong>

## Nesting Elements

One element can be placed inside another. This is called **nesting** elements. For example, if we wanted to make the "Hello World!" text bold and not effect the other text we could do the following:

Code:
```html
<p><strong>Hello world!</strong> This is my first line of HTML!</p>
```

Results:
<p><strong>Hello world!</strong> This is my first line of HTML!</p>

Make sure that the tags close in a way that it's clear one of them inside the other. 

```html
<strong><p>Hello world!</strong> This is my first line of HTML!</p>
```
In this case the browser would have to guess what is going on and that could leading to unexpected results

## Block Vs Inline Elements

**Block-level elements** form a visible block on the page. They start on a new line from the element that precedes them and the elements that follow them start on a new line. Block-level elements are usually structural in nature and some examples include headings, paragraphs, lists, navigation menus and footers. A block-level element would be nested in an inline element but might be nested in another block-level element

**Inline elements** are contained with block-level elements. They do not cause a new line to appear and are usually used with text. Some examples are `<a>` `<em>` and `<strong>` tags 

HTML5 has new [content categories](https://html.spec.whatwg.org/multipage/indices.html#element-content-categories). These categories are more accurate and less ambiguous than block and inline, but also more complicated.

## Void Elements

**Void elements** don't follow the opening tag, content, closing tag anatomy that most element do. The consist of a single tag and are usually used to embed something in the document. 

```html
<img
  src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png" alt="Firefox icon" />
```

This img tag would display like so:

<img
  src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png" alt="Firefox icon" />

  Note that the final slash before the closing greater than symbol is not required, but is useful is you want your html to also be valid XML

  ## Attributes

  ![Attribute Visual](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started/grumpy-cat-attribute-small.png)

  `class` is an attribute that contains a name used to target an element for style information

  Attributes should have 3 things:

  * They should be separated by a space from the preceding tag name or other attribute
  * the attribute name and equal sign (these should not be separated by a space)
  * the attribute value wrapped in quotes

  A **Boolean Attribute** is a type of attribute that is written without a value. It is either listed as an attribute and turned on or not listed and turned off. One example is the `disabled` attribute you can use to disable form elements.

You may see code with attribute values not wrapped in quotes. This is valid in some instances but it is better to avoid and just wrap all values in quotes.

You may use single quote or double quotes to wrap values this is really a matter of preference. The important thing is that you are consistent pick one or the other stick to it throughout the document for readability

## Anatomy of an HTML document

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <title>My test page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>
```

* `<!DOCTYPE html>` is required at the top of every HTML document for correct functionality. It is an historical artifact left over from the early days of HTML
* The `<html></html>` element wraps all other elements in the document. It is also known as the root element
* The `<head></head>` element wraps everything you want to include in an HTML document that isn't the content that the page shows to viewer. This include css style, character set declarations, a description for search engines and more.
*`The <meta charset="utf-8">` the meta tag is used to set meta data that can not be handled by other element like style, and title. The charset attribute sets the character set for the document. UTF-8 is a universal character set that will allow your document to handle almost any type of text it encounters
* The `<title>My test page</title>` element sets the title for the page. It is shown in the tab for the page. It is also used to describe the page if it is bookmarked
*The `<body></body` Include all content that is displayed on the page. All of it!

All sections of **whitespace** in HTML are reduced to sing space when the code is parsed. So most whitespace is completely optional. It is only important for readability. You should use white space in your code to organize and make it logical to other reader and your future self. This is an important idea in all of coding and not just for HTML. For example nested elements should be indented deeper than their parents and siblings should have the same level of indentation.

HTML **entities** are for using characters that are part of the HTML syntax in regular text. They start with a ampersand `&` that is followed by a sequence of characters to represent the actually character you are trying to use. Here is a list of different characters and their entities: 

Literal character	Character | reference equivalent
:--------------------------:|:-------------------:|
`<`                         | `&lt;`
`>`                         | `&gt;`
`"`                         | `&quot;`
`'`	                        | `&apos;`
`&`	                        | `&amp;`

Example of their use:

```html
<p>In HTML, you define a paragraph using the <p> element.</p>

<p>In HTML, you define a paragraph using the &lt;p&gt; element.</p>

```
<p>In HTML, you define a paragraph using the <p> element.</p>

<p>In HTML, you define a paragraph using the &lt;p&gt; element.</p>

HTML **comments** are used to put notes in your code to your future selves and others developers reading your code. The are only in your and your browser will ignore them and they will not be rendered to the screen. Comments are an element of every language I can think of and HTML is no different

To make a comment wrap the comment in `<-- Comment Here -->`

```html
<p>I'm not inside a comment</p>

<!-- <p>I am!</p> -->
```

<p>I'm not inside a comment</p>

<!-- <p>I am!</p> -->


## Metadata in HTML

HTML metadata is contained in the `<head>` elements and includes information that is used by your browser to display your page, It is information that is not rendered to the screen itself such as links to css stylesheets and cdns, the title of the page and important keywords that describe the page, and other information the browser need to display your page correctly

## What is the HTML Head? 

The `<title>` element contains the title of the web page. This title is shown in the tab of the web browser and is the recommend title for bookmarking the page. Used in web search as well.

The `<meta>` tag is used for describing specific meta data about you document. There are many ways of using this tags but some common examples are: 

**Character Encoding**

`<meta charset="utf-8">` UTF 8 is a common character set that includes pretty much every possible character from every human language.

**Author and Description**
```html
<meta name="author" content="Chris Mills" />
<meta
  name="description"
  content="The MDN Web Docs Learning Area aims to provide
complete beginners to the Web with all they need to know to get
started with developing web sites and applications." />

```
Using keywords in your description can help with SEO and Adding an author can tell website users who to contact about the page and is used by CMS's to extract that information

**Favicons**

Favicons stands for favorite icons they can be included in your head element and added to your page

A favicon can be added to your page by:

Saving it in the same directory as the site's index page, saved in .ico format (most also support favicons in more common formats like .gif or .png)

Adding the following line into your HTML's <head> block to reference it:

```html
<link rel="icon" href="favicon.ico" type="image/x-icon" />
```
**Javascript and CSS**

You can use CSS to style your document and javascript to add interactivity. A link or script will need to be added to your `<head>` element like: 

CSS StyleSheet

```html
<link rel="stylesheet" href="my-css-file.css" />
```
Javascript script

```html
<script src="my-js-file.js" defer></script>
````
the defer attribute will defer loading the script until the all the html has been parsed. This will keep you from having javascript errors before the page has a chance to load
**Primary Language**

You can add a primary language to your HTML document with:

```html
<html lang="en-US">
  …
</html>
```
This will help search engines index your page and let screen reader know which language you are using

## HTML Text Fundamentals


## Things I Want to Know More About

* Basic CSS
* Semantic HTML elements
* UX Design Concepts

**references** 

* [MDN HTML COURSE](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)