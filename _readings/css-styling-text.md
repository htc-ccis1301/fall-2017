---
title: "Styling Text"
summary: "An introduction to basic CSS syntax and CSS properties that can be used to change the color of elements on a page."
---

# {{ page.title }}
{{ page.summary }}

## Fonts
One of the most common things that you'll do to style a website is choose specific fonts that match the look that is desired for your page. But before we actually use this, it's helpful to have a general understanding of what fonts are available and how these fonts are used by web browsers.

### Font Categories
Fonts fall into 2 main *visual* categories: serif and sans-serif. Serif fonts have little marks at the tips of the letters and tend to look more formal and are often used for headings.  Sans-serif fonts tend to be used when a lot of text content is displayed for reading.  Sans-serif content is generally considered easier to read.

{% include img-medium.html url="/assets/images/css-styling-text/font-serifs.png"
    alt="Image showing serifs on letters." caption="Image adapted from [Wikipedia](https://en.wikipedia.org/wiki/Sans-serif). Original images created by David Remahl."
%}

There are also monospace, cursive and fantasy fonts, but these are less commonly used.  These font categories are typically used only for small sections of text, such as headings or quotes, or perhaps for code snippets in an IT related page.  

We can also categorize fonts into groups based on how the fonts are accessed by the web browser. Some fonts, called __web safe fonts__, are recognized by web browsers as fonts that are commonly available from the client computer's operating system. While other fonts, called __web fonts__, are downloaded by the browser from the Web when needed.

#### Web Safe Fonts
Most websites rely on fonts that are already installed on the client computers.  However, there is no common set of fonts available on all computers; the fonts available vary based on the operating system of the computer.  To aid with web site design, lists of __web safe fonts__ have been created that include fonts that are pre-installed by *many* operating systems. These lists group those fonts into *font stacks* which are a set of fonts that look similar and cover the major operating systems.


#### Web Fonts
Unlike web safe fonts, __web fonts__ are not pre-installed on the user's system. These fonts are downloaded by the browser from the internet when rendering the webpage.  Because they require a download, these fonts will slow down the initial display of your website.  These fonts are also not supported in older browsers which do not support CSS3.  To avoid issues with older browsers, the best practice is to use a web safe font stack with a web font added as the first font in the list. If a browser is unable to use the web font it will fall back on the web safe fonts in the stack.

### Tools
[CSS Font Stack](http://www.cssfontstack.com/) is a great common font reference.  It will show you font availability for different operating systems and provides good fall back options for when a font is unavailable.

{% include alert.html type="danger"
   content="When adding `font-family` CSS to your web pages, I will expect that you have specified either a proper web safe font stack from [CSS Font Stack](http://www.cssfontstack.com/) or a [Web Font](http://www.cssfontstack.com/Web-Fonts) with appropriate fall-back fonts."
%}

This short video will introduce you to using both [CSS Font Stack](http://www.cssfontstack.com/) & [Lorem ipsum](http://www.lipsum.com/) - a site to get fancy dummy text.

{%  include youtube-16x9.html  id="7gz4_ZWFVFo" %}

### CSS Font-Family
The CSS `font-family` property allows us to specify what font we want the browser to use for particular content. When we specify a font-family, we specify a series of fonts, providing fall-backs in case the first font in our list is not available. While this is more important when using Web Safe Fonts, it is also a good practice when using Web Fonts or Custom Fonts (which we will discuss later).

Here is an example using a *full font stack* for the "Avant Garde" font from [CSS Font Stack](http://www.cssfontstack.com/):
{% highlight CSS %}
body {
  font-family: "Avant Garde", Avantgarde, "Century Gothic", CenturyGothic, AppleGothic, sans-serif;
}
{% endhighlight %}

While you can select fall-back fonts yourself, it is much easier to use a tool like [CSS Font Stack](http://www.cssfontstack.com/). A good font-stack balances the desired appearance with availability on different operating systems.

Here is an example that uses a few different font stacks for different elements on the page.
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="RZdZYL" height="350" tab="css"
%}

### More Font Properties
In addition to specifying which font we want to use, we can also control the font size, weight and style. We'll explore each of these properties individually below.

#### Font Size
The `font-size` property is used to alter the size of the font. Font sizes can be specified in a few different types of units. The most common are pixels (px) and em. The em unit is a relative sizing which adjusts the size of an element relative to the size of its parent element. You can read more about the details of the font-size property on the [CSS-Tricks: CSS Almanac - font-size](https://css-tricks.com/almanac/properties/f/font-size/) page.  

While older websites tend to set font sizes in pixels, the trend toward responsive design has put more focus on relative font sizes using em units. Using this type of sizing also helps when visitors zoom in or out on the web page using the browser.  (Try doing either CTR + or - (or CMD + or - on a Mac) when looking at a web page.)

In the following example, relative font-sizes are specified using em units. The body is set to have a font-size of 16 pixels, and all the other font sizes are relative to this. For example, the h1 is 2em or 2*16 pixels or 32 pixels.

{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="mMoBVK" height="350" tab="css"
%}

#### Font Weight
The `font-weight` property affects the boldness (or lightness/darkness) of the text. Generally you'll just see this used to mark text as bold, but you can also give numeric values for the font-weight.

{% highlight CSS %}
span {
  font-weight: bold;
}
{% endhighlight %}

You can read more about the details of the font-weight property on the [CSS-Tricks: CSS Almanac - font-weight](https://css-tricks.com/almanac/properties/f/font-weight/) page.


#### Font Style
The `font-style` property is used to *italicize* text, or make it appear slanted. Valid values are `normal`, `italic`, and `oblique`.

{% highlight CSS %}
span {
  font-style: italic;
}
{% endhighlight %}

You can read more about the details of the font-style property on the [CSS-Tricks: CSS Almanac - font-style](https://css-tricks.com/almanac/properties/f/font-style/) page.

## More Text Styling
There are many more CSS properties that can be applied to style text, but we'll just focus on a few of the more useful ones. Check them out using the links below to the [CSS-Tricks: CSS Almanac](https://css-tricks.com/almanac/)

- [text-align](https://css-tricks.com/almanac/properties/t/text-align/)
- [text-decoration](https://css-tricks.com/almanac/properties/t/text-decoration/)
- [text-transform](https://css-tricks.com/almanac/properties/t/text-transform/)

Here is an example that applies various CSS rules to style the text:

{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="ZJPJvN" height="480" tab="css"
%}


## CSS for Lists
We can also use the CSS `list-style` property to alter the display of lists. Read more about the details of the list-style property on the [CSS-Tricks: CSS Almanac - list-style](https://css-tricks.com/almanac/properties/l/list-style/) page.

Two common uses of the `list-style` property are to change the list bullet style or convert the bullet to an image.  This is done using the `list-style-type` and `list-style-image` sub-properties. We can also remove the bullets entirely by setting `list-style-type: none`.

Here is an example that applies various CSS rule to style lists:

{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="EvMwRv" height="350" tab="css"
%}


## Review Questions

 - What is the difference between a serif and sans-serif font?
 - What is meant by a font stack?
 - What is the difference between web safe fonts and web fonts?
 - What are the CSS properties used to bold, underline, and italicize text?
 - How do you center text using CSS?
 - How do you change the marker used in an unordered list?
 - How do you change an ordered list to use Roman numerals?
