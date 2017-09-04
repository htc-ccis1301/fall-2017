---
title: "Styling with CSS"
summary: "An introduction CSS (Cascading Style Sheets) and how CSS is used to style, or enhance the display of a web page."
---

# {{ page.title }}
{{ page.summary }}

## Introducing CSS
In the earlier reading, we introduced HTML which is the markup language used to structure and describe content for the web. HTML describes content as being a heading or paragraph or an image. While web browsers have default rules that manage how particular types of content should be displayed, it is often bland and uninteresting. Imagine if all the content on the web was laid out as nothing but black and white pages of text, all with the same text style (or font) with occasional images interspersed between paragraphs. That Web would most likely not be as popular as the one we know today.

It is CSS that is responsible for the amazing amount of variation found in web pages today. CSS stands for Cascading Style Sheets. CSS is a presentation language used to alter the appearance of HTML content. It is a series of rules that tell web browsers how particular content should be displayed.

HTML & CSS are independent languages that serve different purposes. HTML describes the content, giving it a *semantic* meaning. While CSS describes how content should be presented.

To make our websites easier to understand and maintain, it is important to keep our HTML & CSS separate. This is often called a __separation of concerns__. HTML is concerned with describing content, and CSS is concerned with the display of content.  These are independent concerns and the more that they are kept separate, the easier it is to understand and make changes to a web site's content and design.  

## CSS in Action
CSS allows us to apply different fonts and font styles, colors, and layout to our web pages. This can cause the exact same HTML markup to be rendered (or displayed) in the browser in many different ways.  This is a very powerful feature!

To see how powerful, let's look at some examples from the [CSS Zen Garden](http://www.csszengarden.com/) website.  All four images below represent the exact same HTML content, but with different CSS applied to alter the display.

<div style="background-color: #BBB; margin-bottom: 15px;">
<div class="row" style="margin: 15px;">
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
    <a href="http://www.csszengarden.com/">
    <img class="img-responsive" src="{{ "/assets/images/css-intro/basic-css-zengarden-main.png" | prepend:site.baseurl }}"
        alt="A light green watercolor view of the CSS Zen Garden website.">  
    </a>
</div>
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
<a href="http://www.csszengarden.com/216/">
<img class="img-responsive" src="{{ "/assets/images/css-intro/basic-css-zengarden-fk.png" | prepend:site.baseurl }}"
    alt="A sunset colored vintage look for the CSS Zen Garden website.">  
</a>
</div>
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
<a href="http://www.csszengarden.com/221/">
<img class="img-responsive" src="{{ "/assets/images/css-intro/basic-css-zengarden-midcent.png" | prepend:site.baseurl }}"
    alt="A bold retro style for the CSS Zen Garden website.">  
</a>
</div>
<div class="col-sm-6 col-md-5 col-md-push-1" style="padding: 5px;">
<a href="http://www.csszengarden.com/215/">
<img class="img-responsive" src="{{ "/assets/images/css-intro/basic-css-zengarden-robot.png" | prepend:site.baseurl }}"
    alt="A light colored style of the CSS Zen Garden website featuring a robot.">  
</a>
</div>
</div>
</div>

This illustrates some very dramatic formatting and layout changes that can be applied through the use of CSS.  It is almost unbelievable to think that all of this pages use the exact same HTML! In addition to formatting and layout, CSS also supports gradients, transparencies, animations and transitions.  

You'll get the hang of HTML in no time, but becoming a true master of CSS will take much longer.  There is a lot to learn; so don't let that discourage you.

## Basic CSS Syntax
CSS is structured as a series of rules. Each rule is made up of a __selector__ that identifies which content the rule should be applied to, and a __declaration__ that defines how that content should be displayed.  The selector is placed before the curly braces { }, and the declaration is placed inside.  The declaration is make up of one or more property/value pairs.

The first two CSS properties that we'll learn will alter the color of the element when it is displayed in the browser.  

- `background-color` - alters the background color of an element
- `color` - alters the *foreground* color of an element, this generally means its text content

Let's look at a basic example:
{% highlight css %}
body {
    background-color: blue;
}
{% endhighlight %}

Here the selector is `body`.  The declaration is the part in the curly braces or { }. In the declaration, the `background-color` property is specified with the value of `blue`.  This rule will change the background color of the entire web page to blue.

We can also add multiple properties to a single selector. Now the web page background is blue and the text is white.
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="brZGRg" height="340" tab="css"
%}


### Selector Types
In the example shown above, all of the selectors should be recognizable as HTML tag names.  Selectors can also be class or id selectors.  You can also combine multiple selectors and types to make a more specific selector.

|  `body`   | &nbsp;&nbsp;  an HTML selector  &nbsp;&nbsp; |  &nbsp;&nbsp; selects the `body` element
|  `#content`   | &nbsp;&nbsp;  an ID selector  &nbsp;&nbsp; |  &nbsp;&nbsp; selects the item with the `id="content"`
|  `.myClass`   | &nbsp;&nbsp;  a class selector &nbsp;&nbsp; | &nbsp;&nbsp; selects all elements that have `class="myClass"`
| `#content p`  | &nbsp;&nbsp;  a descendant selector &nbsp;&nbsp; | &nbsp;&nbsp; selects all p elements *inside* the element with `id="content"`

### Div & Span
There are two HTML elements that are generally used only to apply CSS to content: `div` and `span`. They are often used with either an `id` or `class` attribute to target content for styling.

The `div` element is a __block__ element, meaning that it has whitespace above and below it separating it from the content before and after it. Other block elements that we have introduced are are headings, paragraphs, and lists. The `span` element on the other hand is an __inline__ element, meaning that it is in-line with other content in the same block. (Read more about block vs inline content on the [Quirksmode - display declaration](https://quirksmode.org/css/css2/display.html) page.)

You'll see `div` and `span` used in many of the CSS examples throughout this module.
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="qXgePN" height="380"
%}


## Adding CSS to HTML
There are a few ways that CSS can be added to an HTML page. We will explore each of these in more depth below and in the Experience: [CSS Cascade]({{ "/experiences/css-cascade.html " | prepend: site.baseurl }}).

- External - written in a separate CSS file and added to HTML using the `link` element
- Embedded - added to a page using the `style` element
- Inline - added to a single element using the style attribute

The last two ways, embedded and inline, are generally considered bad practices because they mix the CSS into the HTML file directly. This makes it difficult to keep the styles consistent across different pages of a site making maintenance and enhancements more difficult. It quickly becomes an unmanageable practice for a large website.

Keeping all CSS separate from the HTML, in external CSS files is a web development best practice. This makes it easy to keep styles consistent across a website as you simply include the same CSS files on all pages. If a particular page needs special styling, an additional file can be included to handle the changes.

{%  include alert.html type="info"
    content="The use of external stylesheets will be required for all assignments in this course unless it is explicitly stated to use inline or embedded styles."
%}

### External CSS
A CSS file is written as a series of rules, one after the other. The rules are read in and applied top to bottom, and as we will see later, the order of these rule can be important because of this.

A simple CSS file might look something like this:
{% highlight HTML %}
body {
  background-color: #271537;
  color: #C493EE;
}

h1 {
 color: #FFFFFF;  
}

h2, h3, h4, h5, h6 {
  color: #D247AC;
}

a {
  color: #8D4CC5;
}
{% endhighlight %}

While it is possible to put multiple CSS properties on a single line of a CSS file, it can make the file harder to read. It is a formatting best practice to only include one property (and its value) on each line. This makes the properties applied in each rule stand out better, and the file is overall easier to read.

To apply the CSS that you've written to an HTML file, you need to link it together using the HTML `link` element. The `href` attribute must specify the *path* to your CSS file.
{% highlight HTML %}
<link rel="stylesheet" href="style.css">
{% endhighlight %}

The `link` element should be placed inside the `head`.
{% highlight HTML %}
<head>
  <title>My Page</title>
  <meta charset="utf-8">
  <link rel="stylesheet" href="style.css">
</head>
{% endhighlight %}

### Embedded CSS
CSS can be applied to an HTML page by adding a `style` element containing CSS rules to the page. The following example, notice that the CSS embedded in the style rule is written the same way it would be if found in an external CSS file.

{% highlight HTML %}
<style>
body {
  background-color: #666666;
  color: #FFFFFF;
}
</style>
{% endhighlight %}

Again, this can be used to handle special exceptions to standard formatting, but it is a better practice to create a separate HTML stylesheet and/or use style classes instead.

### Inline CSS
CSS can be applied to a single element by putting a CSS rule declaration, without the {}, directly into the value of the style attribute. In the following example, notice the style is applied directly to the first `h2` element and does not affect the appearance of the second `h2` element.

{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="zdbZxQ" height="380"
%}

While this can be used to handle special exceptions to standard formatting, it is a better practice to create a style class in an external CSS file and apply that to the element instead. This keeps the HTML markup and CSS presentation separate, and when another exception comes up, the style class can easily be reused ensuring consistent styling.



## CSS Validation
Validation of CSS files is done in much the same way as HTML, only using a different validator.

- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/) - used only for CSS
- [W3C HTML Validator](https://validator.w3.org/) - used only for HTML

Let's use this to validate the CSS used for my [Ice-Cream is Awesome!]( https://htc-ccis1301.github.io/demo-ice-cream/ ) page.

Open the [W3C CSS Validator]( https://jigsaw.w3.org/css-validator/ ) and make sure that you are on the Validate by URI tab.

Next, copy this URL: https://htc-ccis1301.github.io/demo-ice-cream/ and paste it into the Address field on the form.  Then click the Check button.

{% include img-medium.html url="/assets/images/css-intro/css-validation.png"
    alt="Image of Validate by URI tab showing the URL pasted in so we are ready to validate."
%}

Note that with Validate by URI tab of the CSS validator, you may enter either:

1. The URL of your CSS file itself.
2. The URL of an HTML page that uses your CSS file.

In the example above, we used the URL of the HTML page, as it is easy to get to. I recommend that you use this approach when validating the CSS for your assignments.

## Review Questions
 - Explain the syntax of a CSS rule.
 - What does the CSS color property alter?
 - What is the HTML `style` attribute used for?
 - How do you add an external style sheet to a web page?
 - Name four types of CSS selectors.
 - What are the `div` and `span` elements used for?
 - How are `div` and `span` different?
 - How do we validate our CSS?  How is this process similar to the process for validating HTML?  How is it different?
