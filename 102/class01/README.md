# Markdown Notes

GitHub Flavored Markdown(GFM) helps you to format your text in a .md file on GitHub. You can use Markdown to add links, images, youtube videos, and other content into your document. It also let you decorate your text and format it logically with headings, paragraphs, tables, and lists. You can also insert code blocks, block quotes, footnotes, and more. You also might want to checkout the [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) that these notes are based on and the [GFM Specs](https://github.github.com/gfm/) for further reference. 

Thanks for reading and if you like anything about these notes you can always [!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/cannontech) so I can stay up and write more helpful notes for you guys. Thanks for your support.

## Headings

Markdown has 6 choices for headings. A heading should start with pound signs (1-6), followed by a space and then the text for your heading. One preceding pound sign results in the largest heading six pounds results in the smallest.

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
You add italics (emphasis) by wrapping your text in *asterisks* or _underscores_.

Bold (strong emphasis) is added by wrapping your text in double **asterisks** and __underscores__

or you can combine the two with **asterisks and _underscores_**.

you can also add strike through text with tildes. ~~Scratch this.~~
```

You add italics (emphasis) by wrapping your text in *asterisks* or _underscores_.

Bold (strong emphasis) is added by wrapping your text in double **asterisks** and __underscores__

or you can combine the two with **asterisks and _underscores_**.

you can also add strike through text with tildes. ~~Scratch this.~~

## Lists

Ordered list items are proceeded by a number and a period. Unordered list items can start with *, +, or -

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

Images, like links, have reference style and inline style. Inline style images start with an exclamation point, square brackets enclosing the alt text and then the URL or relative path to the image surround by parentheses. Reference style images start with the exclamation and alt text but then have the reference name (Arbitrary and chosen by you) surrounded by square braces. The image url can be placed later in the document as show below.

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
Code blocks are surround by triple backticks

```
insert code here
```
**syntax highlighting**

With some markdown renderers, code blocks offer syntax highlighting for many programming languages and other types of code. To add syntax highlighting for a code block just write the name of the language after the triple backticks but before the new line. How you specify the language may differ from renderer ot renderer if they support it all.
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

## Footnotes

Footnotes aren't officially part of markdown, but are supported by GFM. To make a footnote use square brackets with a caret symbol and a number or word to link to the reference.
'
```markdown
Your first footnote[^1]

Another footnote with multiple lines in the description[^2]

And finally using a word instead of a number[text]

[^1]: I did it!
[^2]: if you want to use more than one line
  be certain to include 2 spaces after each line break
[text]: I told you that you did'nt have to use numbers
```
Your first footnote[^1]


Another footnote with multiple lines in the description[^2]

And finally using a word instead of a number[text]

[^1]: I did it!
[^2]: if you want to use more than one line
  be certain to include 2 spaces after each line break
[text]: 
    I told you that you did'nt have to use numbers. They will still show up numbered in your text
    but this can make it easier for you (the author) to identify. You can also use this 
    "4 spaces after the newline" syntax

## Things I want to learn more about

* block quotes
* code
* images
