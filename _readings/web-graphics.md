---
title: "Web Graphics"
summary: "An introduction to graphic file types and how to add graphics and images to web pages to make the content more interesting & appealing."
---


# {{ page.title }}
{{page.morea_summary}}


## Images on the Web
Let's start with a bit of background information on how images are created, stored and displayed.

{%  include youtube-16x9.html  id="15aqFQQVBWU"
    caption="Thanks to [Code.org](https://code.org) for sharing the video!" %}


## File Types
There are many different image file types currently in use on the Web, and each file type encodes the data representing the image differently. Each file type supports different features and some are best used for specific purposes. A basic understanding these differences is very helpful when creating and using images on the Web.  

### Common Image File Types  

- gif - best used for simple images or line drawings with solid colors, i.e. icons & logos. Limited to 256 colors, but supports transparency & lossless compression.  There are also animated GIF images which consist of several frames that repeatedly cycle making the a simple animation.

- jpeg - best used for photographs.  It supports millions of colors, but not transparency. File sizes of high quality can be large and image quality degrades as the amount of compression increases.

- png - combines the best of gif & jpeg features. It supports lossless compression, with millions of colors, and transparency.

It is important to understand the features provided by each file type. This allows you to choose the best file type for your needs. For example if you need an icon that will look good on several different colored backgrounds, it is helpful to have an image that supports transparency.  This means that either a GIF or PNG would be appropriate, but a JPEG would not as it does not support transparency.  



### HTML Image Element
The image element, the `<img>` tag, is the main method of including graphics on your web site.  The `img` element is always used with the `src` and `alt` attributes. They are both required for valid HTML.

The `src` attribute specifies the location of the image. This is usually a relative path to a file that is part of your website, but might also be a full web URL to a file on another site or server.  The `alt` attribute is used to provide a text description of the image. It is used by screen readers and also shown when the image is not found or cannot be displayed.

Here is an example:

{% highlight html %}
<img src="images/bart.png" alt="Image of the fluffy grey Bart cat.">
{% endhighlight %}

{% include alert.html type="warning"
   content="__Remember to use relative paths for your images when needed.__  
   Images are often kept in a folder just for images. If you do this, you must include the folder name in the path."
%}

Here is the actual image on the page.   

<img src="{{ "/assets/images/web-graphics/bart.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat.">


The image above is shown full-sized, meaning it is presented using the size and dimensions of the actual image file.  This is a 760 pixel square image.  It's a little big for the page. We can reduce the size of the image on the page using HTML attributes for `width` and `height` or by specifying the `width` and `height` in our CSS.  If you do this, be careful not to alter the aspect ratio, distorting the image.

Here is an example resizing the image to 300 pixels, square. Notice that it fits much nicer into the page at this size.

{% highlight html %}
<img src="images/bart.png" alt="Image of the fluffy grey Bart cat." width="300" height="300">
{% endhighlight %}


<img src="{{ "/assets/images/web-graphics/bart.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat." width="300" height="300">

If we do not maintain the correct ratio between the width and height, the image is distorted. Here the height is 150 pixels, but the width is 300 pixels.

{% highlight html %}
<img src="images/bart.png" alt="Image of the fluffy grey Bart cat." width="300" height="150">
{% endhighlight %}

<img src="{{ "/assets/images/web-graphics/bart.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat." width="300" height="200">

Notice the distortion in the image.  Bart is squished.  He would not be happy with this.

We can also resize images using CSS. While we can specify the image size in pixels in the CSS, just like in the HTML, we can also use other dimensions in the CSS rules. Often it is convenient to use a percentage based size.  

In the example below, the Bart image is set to 25% of the width, a relative size.  Notice that if you make your browser window bigger or smaller the size of the image itself changes so that it always takes up 1/4 of the available width.

{% highlight html %}
<img id="bart" src="images/bart.png" alt="Image of the fluffy grey Bart cat.">
{% endhighlight %}

{% highlight css %}
#bart {
  width: 25%;
}
{% endhighlight %}

<img src="{{ "/assets/images/web-graphics/bart.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat." style="width: 25%;" >

In the example above, we only specified the width and the browser determined the correct height based on the aspect ratio of the image file.  

Read more about the CSS width and height properties on CSS Almanac:

- [width](https://css-tricks.com/almanac/properties/w/width/)
- [height](https://css-tricks.com/almanac/properties/h/height/)

### Important Note on Image File Sizes
While *can* adjust image sizes both with the HTML and CSS, it is important to be considerate when doing so.  Consider the image file size and the download time required for that image and any others that will be shown on the page. You don't want to make visitors download a large, 10,000 pixel, photo quality image if you are only showing it at 300 x 300 pixels.  

Always edit your images to reflect a reasonable size and image quality for their purpose on your website.

## Figures & Captions
With HTML5 we have new options for adding images with associated captions.  This uses the `figure` and `figcaption` elements. Please read more about captioning images in this article: [The Correct Way to Markup an Image and Caption in HTML](https://tosbourn.com/correct-way-markup-image-caption-html/).

You should note that you can also use these elemets to caption other types of content this way, not just an image.  For example you might also use this to caption a video, a report or an animation.


## Thumbnails & Image Links
Thumbnail images are also commonly used, particularly with photographs, to allow visitors to your page to preview an image without downloading a large file and waiting for the load time.  A __thumbnail__ is a very small image (hence the name *thumbnail*, as in thumbnail sized). There is no official size for a thumbnail, and it is not usually really the size of an actual person's thumbnail. However somewhere around 100 - 200 pixels is generally acceptable.  

Thumbnails usually link to a larger version of the same image. This allows you to get a sense of what the image is, allowing you to decide if you want to click the link to view the larger image. Using smaller images (with smaller file sizes) helps with your web page's load time. However the image quality generally suffers with the smaller, lower quality image. Thumbnails aim to find a balance between the two.

Here is an example of a thumbnail image linking to a larger image.  The HTML code is shown here.
{% highlight html %}
<a href="images/bart.png">
  <img src="images/bart-thumbnail.png" alt="Thumbnail sized Bart cat.">
</a>
{% endhighlight %}

Here is the actual thumbnail image on the page.   

<a href="{{ "/assets/images/web-graphics/bart.png" | prepend:site.baseurl }}">
  <img src="{{ "/assets/images/web-graphics/bart-thumbnail.png" | prepend:site.baseurl }}" alt="Thumbnail sized Bart cat.">
</a>

Note that you can click on the *thumbnail* image shown above to go to a full-sized version of the image.


### Background Images
It is important to remember that background images should only be used for decorative elements on your page. This is because images added with CSS do not have alternative text representations for accessibility and fallback when the file is unavailable.

{% include alert.html type="danger"
   content="Any images with *meaning* MUST be added using the HTML `img` element to provide `alt` text for accessibility and fallback."
%}

Background images can be applied to any HTML element using CSS.  For example, you might configure a background image for the body tag to make the entire web page background look like a piece of aged paper.  You might also put just a small image in the background in a particular position, like the bottom right.  

Key CSS properties for using background images are listed below with links to further information.

- [background-image](http://css-tricks.com/almanac/properties/b/background-image/)
- [background-repeat](http://css-tricks.com/almanac/properties/b/background-repeat/)
- [background-position](http://css-tricks.com/almanac/properties/b/background-position/)
- [background-size](http://css-tricks.com/almanac/properties/b/background-size/)

The best way to begin to understand how these properties work is to experiment with them.  Create a simple page and add a background image using the properties above.  Experiment with changing the values and see how the display of the image on the page is affected by the changes to the properties.

### Examples
Let's use a background-image behind a section of page text.  The image is of grungy paper.  You can see the full image here: [Grungy-paper]({{ "/assets/images/web-graphics/grungy-paper.jpg" | prepend:site.baseurl }})

#### Example 1
{% highlight css %}
section {
  background-image: url(images/grungy-paper.jpg);
}
{% endhighlight %}

<section style="background-image: url({{ "/assets/images/web-graphics/grungy-paper.jpg" | prepend:site.baseurl }});">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque in commodo ex, id consectetur nunc. Maecenas sit amet ultricies est. Sed interdum dignissim viverra. Etiam nunc dui, dictum sit amet neque semper, pulvinar pellentesque diam. Curabitur venenatis dui imperdiet enim commodo rhoncus. In vitae dolor sed leo dignissim lacinia. Etiam erat elit, eleifend nec ex a, dictum faucibus tortor. Aenean ligula est, rutrum eget volutpat vitae, sollicitudin nec massa. Vivamus bibendum dignissim suscipit. Maecenas nibh ligula, suscipit a rutrum nec, molestie non massa. Quisque risus massa, hendrerit feugiat consectetur vel, tempus pretium neque. Nulla in auctor arcu.
</section>

#### Example 2
Now let's alter the appearance of the background image by changing its position:

{% highlight css %}
section {
  background-image: url(images/grungy-paper.jpg);
  background-position: bottom;
}
{% endhighlight %}

The same image is used behind this section, however it's position is shifted to the bottom.

<section style="background-position: bottom; background-image: url({{ "/assets/images/web-graphics/grungy-paper.jpg" | prepend:site.baseurl }});">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque in commodo ex, id consectetur nunc. Maecenas sit amet ultricies est. Sed interdum dignissim viverra. Etiam nunc dui, dictum sit amet neque semper, pulvinar pellentesque diam. Curabitur venenatis dui imperdiet enim commodo rhoncus. In vitae dolor sed leo dignissim lacinia. Etiam erat elit, eleifend nec ex a, dictum faucibus tortor. Aenean ligula est, rutrum eget volutpat vitae, sollicitudin nec massa. Vivamus bibendum dignissim suscipit. Maecenas nibh ligula, suscipit a rutrum nec, molestie non massa. Quisque risus massa, hendrerit feugiat consectetur vel, tempus pretium neque. Nulla in auctor arcu.
</section>

#### Example 3
Now let's alter the appearance of the background image by resizing it so the entire width OR height image is shown to cover the entire area. This doesn't alter the aspect ratio, but parts of the image may not be shown.

{% highlight css %}
section {
  background-image: url(images/grungy-paper.jpg);
  background-size: cover;
}
{% endhighlight %}

Notice how this is different than the first example's image.  It is similar, but the large dots on the right are smaller and closer to the center of the image. This allows the rest of the right side of the image to be shown.

<section style="background-size: cover; background-image: url({{ "/assets/images/web-graphics/grungy-paper.jpg" | prepend:site.baseurl }});">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque in commodo ex, id consectetur nunc. Maecenas sit amet ultricies est. Sed interdum dignissim viverra. Etiam nunc dui, dictum sit amet neque semper, pulvinar pellentesque diam. Curabitur venenatis dui imperdiet enim commodo rhoncus. In vitae dolor sed leo dignissim lacinia. Etiam erat elit, eleifend nec ex a, dictum faucibus tortor. Aenean ligula est, rutrum eget volutpat vitae, sollicitudin nec massa. Vivamus bibendum dignissim suscipit. Maecenas nibh ligula, suscipit a rutrum nec, molestie non massa. Quisque risus massa, hendrerit feugiat consectetur vel, tempus pretium neque. Nulla in auctor arcu.
</section>

#### Example 4
Now let's alter the appearance of the background image by resizing it so the *entire* image is shown.

{% highlight css %}
section {
  background-image: url(images/grungy-paper.jpg);
  background-size: contain;
}
{% endhighlight %}

It's hard to tell what happened this time, but the image is both squished and repeated.

<section style="background-size: contain; background-image: url({{ "/assets/images/web-graphics/grungy-paper.jpg" | prepend:site.baseurl }});">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque in commodo ex, id consectetur nunc. Maecenas sit amet ultricies est. Sed interdum dignissim viverra. Etiam nunc dui, dictum sit amet neque semper, pulvinar pellentesque diam. Curabitur venenatis dui imperdiet enim commodo rhoncus. In vitae dolor sed leo dignissim lacinia. Etiam erat elit, eleifend nec ex a, dictum faucibus tortor. Aenean ligula est, rutrum eget volutpat vitae, sollicitudin nec massa. Vivamus bibendum dignissim suscipit. Maecenas nibh ligula, suscipit a rutrum nec, molestie non massa. Quisque risus massa, hendrerit feugiat consectetur vel, tempus pretium neque. Nulla in auctor arcu.
</section>

Setting the background-size to contain alters the size so that both the image's height and width fit in the content area. To do this, the image becomes rather small. We can see this more clearly by telling the browser not to repeat the image.

{% highlight css %}
section {
  background-image: url(images/grungy-paper.jpg);
  background-size: contain;
  background-repeat: no-repeat;
}
{% endhighlight %}

Notice now the right side of the text has no image behind it.

<section style="background-repeat: no-repeat; background-size: contain; background-image: url({{ "/assets/images/web-graphics/grungy-paper.jpg" | prepend:site.baseurl }});">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque in commodo ex, id consectetur nunc. Maecenas sit amet ultricies est. Sed interdum dignissim viverra. Etiam nunc dui, dictum sit amet neque semper, pulvinar pellentesque diam. Curabitur venenatis dui imperdiet enim commodo rhoncus. In vitae dolor sed leo dignissim lacinia. Etiam erat elit, eleifend nec ex a, dictum faucibus tortor. Aenean ligula est, rutrum eget volutpat vitae, sollicitudin nec massa. Vivamus bibendum dignissim suscipit. Maecenas nibh ligula, suscipit a rutrum nec, molestie non massa. Quisque risus massa, hendrerit feugiat consectetur vel, tempus pretium neque. Nulla in auctor arcu.
</section>

## Fav Icon
Setting up a favorites icon for your web page can help it to stand out.  If you are like me, and often have 10 or more tabs open, then you'll appreciate those that have a little icon indicating what page it is for.  

{% include img-small.html url="/assets/images/web-graphics/favicon.png"
    alt="Browser tab highlighting favicon location."
%}

The favorites icon is configured with the `<link>` tag.  

{% highlight html %}
<link rel="icon" href="myFav.ico" type="image/x-icon">
{% endhighlight %}

There are internet sites that will create a favicon from an image for you.  One such site is the [Favicon & App Icon Generator](https://www.favicon-generator.org/).

## Review Questions

- Which image file types support transparency?  Which types support animation?
- What attribute is required on the image element for accessibility?
- How do you add a background image to an element when using CSS?
- How would you repeat a background image down the left side of an element?  Across the top?
- How do you generate a favicon and add it to your page?  Where is it shown?
- Explain the use of the background-size, background-position, and background-repeat properties.
