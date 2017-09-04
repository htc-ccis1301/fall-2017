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


## Image File Types
There are many different image file types currently in use on the Web, and each file type encodes the data representing the image differently. These file types support different features and some are best used for specific purposes. A basic understanding these differences is very helpful when creating and using images on the Web.  

For example, if you need an icon that will look good on different colored backgrounds, it is helpful to have an image with a transparency layer.  So a GIF or PNG would be appropriate, but a JPEG would not as it does not support transparency.

Common Image File Types  









### HTML Image Element
The image element, the `<img>` tag, is the main method of including graphics on your web site.  To give images a fixed size, use the `height` and `width` attributes, but be careful not to make visitors download a large photo quality image if you are only showing it at 300 x 300.  You should always edit your images to reflect a reasonable size and image quality for their purpose.

Providing multiple images in different sizes and qualities is a good way to support this.  If you have an image gallery that displays thumbnails and users can click on an image to go to a larger view, make separate images for each.  The thumbnails should be thumbnail sized and lower quality for faster download.  Only if a visitor wants to see the larger more detailed image do they need to download the larger file.

It is easy to make an image a link by wrapping it with an anchor tag.  Again, if you are using these images for navigation, be sure to consider alternative options for accessibility. Use the `alt` attribute to hold the text displayed in the image, and consider adding a set of nav items to the footer where the will be unobtrusive for most users, but provide critical information for screen readers.

### Background Images
It is important to remember that background images should only be used for decorative elements on your page.  Any images with *meaning* should be added using the `<img>` tag with `alt` text.

Background images can be applied to any HTML element using CSS.  For example, you might configure a background image for the body tag to make the entire web page background look like a piece of aged paper.  You might also put just a small image in the background in a particular position, like the bottom right.  

Key properties are:

- background-image
- background-repeat
- background-position


{% include alert.html type="warning"
   content="__Remember to use relative paths for your images.__  
   Images are often kept in a folder just for images. See the note at the bottom of page 149 in your textbook for examples of how to support this."
%}


### Fav Icon & Image Maps
The end of Chapter 5, discusses the favorites icon, which is shown in the browser window or tab next to the title, and image maps, which are images with clickable locations in the image.

Setting up a favorites icon for your web page can help it to stand out.  If you are like me, and often have 10 or more tabs open, then you'll appreciate those that have a little icon indicating what page it is for.  The favorites icon is configured with the `<link>` tag.  

{% highlight html %}
<link rel="icon" href="myFav.ico" type="image/x-icon">
{% endhighlight %}

The information about image maps is good to be aware of, however we will not use or focus on image maps in this course.  When using image maps for a site, it is important to ensure that their use and purpose is obvious to website visitors.  An image with multiple links hidden in it might seem cool, but if people don't realize they can click on different parts of the image, they may be stuck on your home page.  Accessibility is also something to pay special attention to with image maps, especially if they are providing your sites main navigation.

## Review Questions

 - Which image file types support transparency?  Which types support animation?
 - What attribute is required on the image element for accessibility?
 - When using images for navigation, what alternatives are recommended to support accessibility?
 - How do you add a background image to an element when using CSS?
 - How would you repeat a background image down the left side of an element?  Across the top?
 - Can you add more than one background image for the same element?  
 - Explain the term *progressive enhancement*.
