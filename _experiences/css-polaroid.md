---
title: "CSS Polaroid"
summary: "Let's use what we've learned in this module to style an image like a Polaroid."
---

# {{ page.title }}
{{page.summary}}

## Prerequisites
Completion of this exercise requires an understanding of the material presented in the readings:  

- [Web Graphics]({{ "/readings/web-graphics.html " | prepend: site.baseurl }})
- [CSS Box Model]({{ "/readings/css-box-model.html " | prepend: site.baseurl }})
- [Styling for Images & Layout]({{ "/readings/css-more-styles-more.html " | prepend: site.baseurl }})

## A little history
Have you seen any *old-fashioned* Polaroid images? They were a type of camera that produced *instant* photographs. They used to be all the rage, but it's hard to find them now in the age of cell-phone selfies.  You can read more about it and see examples on [Wikipedia: Instant Film](https://en.wikipedia.org/wiki/Instant_film)

## Polaroid an Image
We can use CSS to make an image look like a Polaroid on the web.  To do this we'll need to pull together a few different styles from the readings.

### Setup
To do this exercise, you'll need to have an HTML page with a linked CSS file already set up.

1. Add an image to the web page using the HTML `figure`, `img` and `figcaption` elements as discussed in the reading. It helps to have the image be relatively square in size.

2. Give the image a style class called "polaroid".

### Apply the CSS
In your CSS file, set up a style rule for the "polaroid" class.  

- Set the background color to white
- Add a very dark grey (#444), 1 pixel border around all sides

Notice that the figure's border extends the full width of the page.  

{% include img-small.html url="/assets/images/css-polaroid/too-wide.png"
    alt="Image showing Brackets Live Preview, figure is too wide."
%}

That's not what we want for our polaroid.  We want the width to match the image.  To fix this, set the display to inline-block.

{% highlight CSS %}
display: inline-block;
{% endhighlight %}

{% include img-small.html url="/assets/images/css-polaroid/better-width.png"
    alt="Image showing Brackets Live Preview, figure is correct size."
%}

That's better, but not very Polaroid shaped.  Polaroids have a border around the image.  Let's set that up using margins and padding.

First we'll extend the size on the top and bottom with padding.

- Add 12px padding to the top.
- Add 5px padding to the bottom.

To get the space on the side, we are going to add a margin to the image.

Set up a rule for a __descendant selector__ to get the image *inside* the Polaroid figure.  It's important to use the descendant selector so that we don't select all images on our page. For a descendant selector, use the parent selector first, then a space, and then the descendant selector.  Here it is `.polaroid img`.  That will select all img elements inside any element with a "polaroid" style class.

{% highlight css %}
.polaroid img {

}
{% endhighlight %}

In this new `.polaroid img` rule:

- Add a margin of 8 pixels on all sides.
- Add a super dark grey (#222), 1 pixel border around all sides.

Now you should have something like this.  

{% include img-small.html url="/assets/images/css-polaroid/borders.png"
    alt="Image showing Brackets Live Preview, figure has wide white borders on all sides."
%}

Note that you may need to adjust the sizes of the padding and margin to look good with the size of your image.  My image is about 300 pixels square.


Now let's work on that text.  To make it look authentic, we want the text to appear handwritten.  For this we're going to use a Web Font. To use a Web Font, vs a web safe font, you need to include a link for the browser to download the font from the web.

Add this link to your HTML `head` element:

{% highlight html %}
<link rel="stylesheet" type="text/css" href="//fonts.googleapis.com/css?family=Nothing+You+Could+Do" />
{% endhighlight %}

Now set up another __descendant selector__ in your CSS file to target the `figcaption` inside the polaroid.  It will be similar to what you did for the image, but will target the figure caption instead.

In this new descendant selector for the figure caption:

- Add a font family for our Web Font, that also has web save font fallbacks: `font-family: "Nothing You Could Do", "Brush Script MT", cursive;`
- Increase the font-size to suit the image. I used 1.3em for mine.
- Center the text.

Now you should have something like this.  

{% include img-small.html url="/assets/images/css-polaroid/text-styled.png"
    alt="Image showing Brackets Live Preview, figure has text styling to look handwritten."
%}

This is actually really close, but looks a little fake still.  

We could use a little more space at the bottom, between the text and the image. There's also a light line across the bottom where the film cover peels away.

Inside the figure caption descendant selector:

- Add a pale grey (#EEE), 1 pixel border to the top
- Add a little more padding to the top. About 8 pixels should do.

Now you should have something like this. It should be looking *really* good now.

{% include img-small.html url="/assets/images/css-polaroid/almost-perfect.png"
    alt="Image showing Brackets Live Preview, figure has additional styling to edge the bottom."
%}

The last bit we'll add is some slight rounding to the outside corners, a shadow, and a slight rotation to make it look more real.

Add these styles to the original "polaroid" style rule:

- Add slightly rounded corner, about a 3-pixel radius should do.
- Add a medium grey (#999) box shadow, of about a 3-pixel horizontal & vertical offset with a 2-pixel blur.
- Rotate it a few degrees (1-3), to make it look casually placed.

If you really wanna give it an old feel, use an image editor to darken the image and add more sepia. Some handy photo editing tools also have filters for this, but I just did it with the basic Mac image editor. Don't stress it if you don't have one. It adds a nice touch, but isn't required.

Now you should have an awesome web Polaroid!
{% include img-small.html url="/assets/images/css-polaroid/perfect.png"
    alt="Image showing Brackets Live Preview, with a perfectly styled Polaroid."
%}

Check out my finished work on GitHub: [mbmosman/demo-polaroid-image](https://github.com/mbMosman/demo-polaroid-image)
