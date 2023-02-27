# Images, Color, Text

## Reading Q&A
* **What is a real world use case for the alt attribute being used in a website?**
As a user with a visual impairment I want to read a description of images so I can understand the content of the website with out having to see the images

* **How can you improve accessibility of images in an HTML document?**
Always include a description of the image with the `alt` attribute. Avoid using the `title` attribute as it's behavior with screen readers is unpredictable. Use CSS for background-images where possible and leave the `alt` attribute as `""` for decorative images. We don't want screen readers to read descriptions of images that aren't important for understanding the content.

* **Provide an example of when the figure element would be useful in an HTML document.** You would want to use a `figure` and `figcaption` element whenever you have and image you want to display with a caption. This makes the format of your document more apparent to screen readers. If you have many images with captions the user will know which caption goes with which images.

* **Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.**
Gif is an image file type that was created in 1987. It uses lossless file compression, stores pixel with 24 bit color, and supports simple animations. SVG files contain source code that is used to draw images. SVG is ideal for diagrams, icons, and logos. SVG will scale to desired size and is not useful for bitmaps or photographic images.

* **What image type would you use to display a screenshot on your website and why?**
I would use .jpg because it uses lossy compression and it a good choice for photos. PNG is lossless and that kind of exactness is not needed for a simple screenshot and would take up more file space on my website

* **Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.** Foreground color is the color of your text or other content. Background color is the of your paper. If you were doing arts and craft the colored paper would represent the background color and the color of your marker would be the foreground color.

* **Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?** I would ask him more questions to get an idea of what kind of colors he was looking for. I would then try to create a color palette to match the colors he likes. I would make sure they were followed standards the web like having enough contrast for accessibility. I would then apply the colors using CSS. 

* **What should you consider when choosing fonts for an HTML document?** Are the fonts supported on most browsers? What backup fonts would make sense to use incase of non compatibility and are the fonts readable and considered professional for the type of content on the site. 

* **What do font-size, font-weight, and font-style do to HTML text elements?** font size determines the width and height of the letters. font-weight determines how thick the lines of the letters are and font style determines the writing style or shape of the letters.

* **Describe two ways you could add spacing around the characters displayed in an h1 element.** You could use letter-spacing to specify the horizontal distance between each character and line-height to specify the distant between the lines of text vertically.

## Things I want to know more about