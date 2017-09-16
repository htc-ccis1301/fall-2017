---
title: "Styling for Images & Layout"
summary: "Additional styles for working with images and improving your overall layout and design."
---


# {{ page.title }}
{{page.morea_summary}}

## Transform
There are some neat effects that can be achieved using the CSS `transform` property on your images.

### Rotate
For example, you can get a neat, scrapbook like effect by using the CSS `transform` property to [rotate](https://css-tricks.com/almanac/properties/t/transform/#article-header-id-2) the image.

{% highlight html %}
<img id="bart" src="images/bart.png" alt="Image of the fluffy grey Bart cat.">
{% endhighlight %}

{% highlight css %}
#bart {
  transform: rotate(-5deg);
}
{% endhighlight %}

<img id="bart" src="{{ "/assets/images/web-graphics/bart-thumbnail.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat." style="margin: 15px 0; transform: rotate(-5deg)" >

Note that you can rotate any content, not just images using this CSS property.  

### Skew
You can also get interesting effects using `transform` to [skew](https://css-tricks.com/almanac/properties/t/transform/#article-header-id-1) an image.

{% highlight html %}
<img id="bart2" src="images/bart.png" alt="Image of the fluffy grey Bart cat.">
{% endhighlight %}

{% highlight css %}
#bart2 {
  transform: skewY(20deg);
}
{% endhighlight %}

<img id="bart" src="{{ "/assets/images/web-graphics/bart-thumbnail.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat." style="margin: 15px 0; transform: skewY(20deg)" >

How are they different?  Using skew, the image is no longer square.

### CSS Animation
The `transform` property can also be used to achieve animation effects using only CSS.  This is actually really cool.  I won't ask you to apply transform for animation in this course, but you are welcome to try it out and apply it to your projects as extras if you wish.

Read more about CSS transform and animation on the CSS Almanac: [transform](https://css-tricks.com/almanac/properties/t/transform/)


## Rounded Corners
Rounded corners were a *thing* a few years ago, but the trend more recently has leaned back towards square. The current *buzz* style varies year-by-year and individual style varies site-by-site. If you like the rounded look and it works for your site, use it.  If you (or your customer) prefer the sharp, square corners, use those. Worry more about what works for your site's style than the latest *buzz* trends.

Rounded corners used to be a more difficult thing to achieve.  You needed to actual set them up with images for the corners, with the right background color and position.  It was tricky and made sites stand out a bit more if they could pull it off.  (If you bump into this old-style stuff, be sure to speak up about the newer, better way.)

Today it's simple to set up rounded corners in seconds using CSS. Read more about creating rounded corners with CSS on the CSS Almanac: [border-radius](https://css-tricks.com/almanac/properties/b/border-radius/)

### Example 1 - Image
{% highlight html %}
<img id="bart3" src="images/bart.png" alt="Image of the fluffy grey Bart cat.">
{% endhighlight %}

{% highlight css %}
#bart3 {
  border-radius: 15px;
}
{% endhighlight %}

<img id="bart" src="{{ "/assets/images/web-graphics/bart-thumbnail.png" | prepend:site.baseurl }}" alt="Image of the fluffy grey Bart cat." style="border-radius: 15px;" >

### Example 2 - Heading
{% highlight html %}
<h4 class="rounded">Example Heading</h4>
{% endhighlight %}

{% highlight css %}
.rounded {
  background-color: blue;
  color: white;
  padding: 10px;
  border-radius: 25px;
}
{% endhighlight %}

<h4 style="border-radius: 25px; padding: 10px; background-color: blue; color: white;" >Example Heading</h4>


## Box and Text Shadow
CSS can also be used to configure box and text shadows on elements. Read more about creating these effects on the CSS Almanac:
- [box-shadow](https://css-tricks.com/almanac/properties/b/box-shadow/)
- [text-shadow](https://css-tricks.com/almanac/properties/t/text-shadow/)

A good application of these styles can really make a website *pop* or stand out.  However don't get too carried away with them.  If you start applying it to everything, you just might get dizzy looking at your page.  If everything starts floating off the screen, it can get a little disconcerting.  Use it sparingly for the best effect.

### Example
{% highlight html %}
<h4 class="shadow">Example Heading</h4>
{% endhighlight %}

{% highlight css %}
.shadow {
  text-shadow: 2px 2px 1px #2874A6;
}
{% endhighlight %}

<h4 style="text-shadow: 2px 2px 1px #2874A6;" >Example Heading</h4>





## Review Questions

 - Explain how to rotate an image using CSS?
 - How do you make rounded corners for the border of an element?  
 - How do you set up a text shadow for an element?  
 - Explain the five properties that can be used to set up a box shadow.  Are all required?
