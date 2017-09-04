---
title: "CSS Box Model"
summary: "Understanding the CSS box model is an important aspect of setting up CSS for page layout."
---


# {{ page.title }}
{{page.morea_summary}} The addition of margins, padding and borders can make a huge difference to the look of your page, allowing you to group and space content for better clarity and presentation.  

{% include alert.html type="note" content="Understanding the CSS box model is *very* important to making web pages look good.  Margins and padding are perhaps the two most commonly used styles.  Make sure that you understand the difference between the two, and when using each is more appropriate." %}


## Box Model
The CSS box model shows an element's size, padding, border, and margin.  Remember that the browser developer tools will illustrate the box model for you for a selected element.  In the image below, you can see the element's size (in the blue area in the center), the padding (the inner green area), the border (the yellow area separating the padding and margin), and the margin (the orange outer area).

{% include img-small.html url="/morea/more-css/images/css-box-model-ex.png"  alt="Image of the CSS box model diagram from the Chrome developer tools." %}

Remember that padding picks up the element's background color, while the margin is transparent and thus shows the color of the parent or containing element.

Key properties:
- width and height
- margin (note both the shorthand and individual properties)
- padding (note both the shorthand and individual properties)
- border (note both the shorthand and individual properties)

Understanding the box model and how it affects the layout of HTML elements is important to the layout of your web site.  It controls the size and spacing of elements. Correct use of the opaque (padding) and transparent (margin) can make a big difference in how elements appear on the page.

## More CSS
These are all topics you should be aware of, but may not want or need to memorize.  They're easy to look up if you need them, and aren't used as frequently as others.

Keep in mind that this is all relatively new stuff and you'll want to pay attention to browser support for these features.  Ensure that an acceptable fall-back is in place when these properties are unsupported.

### Rounded Corners
Rounded corners were a *thing* a few years ago, but the trend more recently has leaned back towards square.  The current *buzz* style varies year-by-year and individual style varies site-by-site. Rounded corners used to be a more difficult thing to achieve.  You needed to actual set them up with images for the corners, with the right background color and position.  It was tricky and made sites stand out a bit more if they could pull it off.  (If you bump into this old-style stuff, be sure to speak up about the newer, better way.)

Today it's simple to set up in minutes using CSS.  Perhaps that's why it's less of a trend?  Who knows.  But if you like the look and it works for your site, use it.  If you (or your customer) prefer the sharp, square corners, use those. Worry more about what works for your site's style than the latest *buzz* trends.


### Box and Text Shadow
A good application of these styles can really make a website *pop* or stand out.  However don't get too carried away with them.  If you start applying it to everything, you just might get dizzy looking at your page.  If everything starts floating off the screen, it can get a little disconcerting.  Use it sparingly for the best effect.



## Review Questions

 - Explain the CSS Box Model.
 - What is the difference between margin and padding?
 - Does the margin show the background-color of the property it is applied to?  Does the padding?
 - What options are available when configuring a border for an element?
 - How do you use margins to center block content?
 - How do you make rounded corners for the border of an element?  Is this supported on all browsers?
 - How do you set up a text shadow for an element?  
 - Explain the five properties that can be used to set up a box shadow.  Are all required?
 - Explain the use of the background-clip, background-origin, and background-size properties.
