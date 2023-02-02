# Markdown Notes

GitHub Flavored Markdown helps you to format your text in a .md file on github. You can use mark down to add links, images and other content into your document. It also let you decorate text and format your text logically with headings, paragraphs, and lists. You can also insert code blocks, blockquotes, tables, youtube videos and much more. You also might want to checkout the [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) that these notes are based on and the [GFM Specs](https://github.github.com/gfm/) for further reference. 

Thanks for reading and if you like anything about these notes you can always [!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/cannontech) so I can stay up and write more helpful notes for you guys. Thanks for your support.

## Headings

Markdown has 6 choices for headings. A heading should start with pound signs (1-6), followed by a space and then the text for your heading. One preceding pound results in the largest heading six pounds results in the smallest.

```markdown
# H1

## H2

### H3

#### H4

##### H5

###### H6
```

# H1

## H2

### H3

#### H4

##### H5

###### H6 


You can also use the underline syntax for H1's and H2's like so

```markdown
Alt-H1
======

Alt-H2
------
```

H1
==

H2
--



## Decorating text

```markdown
You add emphasis (italics) by wrapping your text in *asterisks* or _underscores_.

Bold(strong emphasis is added by wrapping your text in double **astericks** and __underscores__

or you can combine the two with **asterisks and _underscores_**.

you can also add strike through text with tildes. ~~Scratch this.~~
```

You add emphasis (italics) by wrapping your text in *asterisks* or _underscores_.

Bold(strong emphasis is added by wrapping your text in double **astericks** and __underscores__

or you can combine the two with **asterisks and _underscores_**.

you can also add strike through text with tildes. ~~Scratch this.~~

## Lists

Ordered list items are preceeded by a number and a period. Unordered list items can start with *, +, or -

```markdown
1. First list ordered list item
    * insert spaces when making a sub list
    - another sublist item
    + and a third
2. Second ordered list item
    1. ordered sublists work as well
```
## Links

There are two styles of links, inline links and reference links. You can either put the link address in the same line as your hyperlink or use a reference address and define the link later in the document

```markdown

**inline style**
[inline-style link](https://www.google.com)

[inline-style link with title](https://www.google.com "Google's Homepage")

**reference style**
[reference-style link][reference text]

[relative reference link ](../blob/master/LICENSE)

[You can use numbers to reference links][1]

Or you can use the [link text itself].

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
```
**inline style**

[inline-style link](https://www.google.com)

[inline-style link with title](https://www.google.com "Google's Homepage")

**reference style**

[reference-style link][reference text]

[relative reference link ](../blob/master/LICENSE)

[You can use numbers to reference links][1]

Or you can use the [link text].

[reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text]: http://www.reddit.com

## Images

Images, like links, have reference style and inline style. Inline style images start with an exclamation point, square brackets enclosing the alt text and then the URL or relative path to the image surround by parentheses. Reference style images start with the exclamation and alt text but then have the reference name (Arbitrary and chosen by you) surroundeded by square braces. The image url can be placed later in the document as show below.

```markdown
**inline style**

![alt text](https://cdn.iconscout.com/icon/premium/png-512-thumb/markdown-4887934-4072470.png?f=avif&w=128)

**reference style**

![alt text][markdown logo]

[markdown logo]: https://cdn.iconscout.com/icon/premium/png-512-thumb/markdown-4887934-4072470.png?f=avif&w=128
```
**inline style**

![alt text](https://cdn.iconscout.com/icon/premium/png-512-thumb/markdown-4887934-4072470.png?f=avif&w=128)

**reference style**

![alt text][markdown logo]

[markdown logo]: https://cdn.iconscout.com/icon/premium/png-512-thumb/markdown-4887934-4072470.png?f=avif&w=128

## Code 

Code can be added either inline or in code blocks.

**inline code** 

```markdown
inline code is surrounded by backticks `insert code here`. 
```
inline code is surrounded by backticks `insert code here`. 

**code blocks**

````markdown
Code blocks are suround by triple backticks

```
insert code here
```
````
Code blocks are suround by triple backticks

```
insert code here
```
**syntax highlighting**

code blocks offer syntax highlighting for many programming languages and other types of code. To add syntax highlighting for a code block just write the name of the language after the tripple backticks but before the new line
````markdown
```javascript
console.log("hello, world!");
```

```python
print "hello, world"
```

```markdown
**hello, world!**
```
````

```javascript
console.log("hello, world!");
```

```python
print "hello, world"
```

```markdown
**hello, world!**
```

don't forget to tell markdown which language you need the highlighting for

````
```
#include <iostream>

int main() {
    std::cout << "You forgot to tell me what language this is dummy";
    return 0;
}
```

```c++
#include <iostream>

int main() {
    std::cout << "oooh pretty";
    return 0;
}
```
````
```
#include <iostream>

int main() {
    std::cout << "You forgot to tell me what language this is dummy";
    return 0;
}
```
```c++
#include <iostream>

int main() {
    std::cout << "oooh pretty";
    return 0;
}
```
## Things I want to learn more about

* block quotes
* code
* images
