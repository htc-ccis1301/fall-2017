---
title: "CSS Box Model"
summary: "Understanding the CSS box model is an important aspect of setting up CSS for page layout."
---


# {{ page.title }}
{{page.morea_summary}} The addition of margins, padding and borders can make a huge difference to the look of your page, allowing you to group and space content for better clarity and presentation.  

{% include alert.html type="note" content="Understanding the CSS box model is *very* important to making web pages look good.  Margins and padding are perhaps the two most commonly used styles.  Make sure that you understand the difference between the two, and when using each is more appropriate." %}


## Box Model
The CSS box model controls an element's size, padding, border, and margin.

__I will not cover this topic in depth here.__

Please read this article from Mozilla on the [CSS Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Box_model)

Understanding the box model and how it affects the layout of HTML elements is important to the layout of your web site.  It controls the size and spacing of elements. Correct use of the opaque (padding) and transparent (margin) can make a big difference in how elements appear on the page.


### Key CSS Properties
Key CSS properties for working with the box model are listed below with links to further information.

- [width](https://css-tricks.com/almanac/properties/w/width/)
- [height](https://css-tricks.com/almanac/properties/h/height/)
- [margin](https://css-tricks.com/almanac/properties/m/margin/) - Note both the shorthand and individual properties. Also note how `auto` margins with a width can be used to center content on the page.
- [padding](https://css-tricks.com/almanac/properties/p/padding/) - Note both the shorthand and individual properties
- [border](https://css-tricks.com/almanac/properties/b/border/) - Note both the shorthand and individual properties

Remember that padding picks up the element's background color, while the margin is transparent and thus shows the color of the parent or containing element.

### Dev Tools Reminder
Remember that the browser developer tools will illustrate the box model for you for a selected element.  In the image below, you can see the element's size (in the blue area in the center), the padding (the inner green area), the border (the yellow area separating the padding and margin), and the margin (the orange outer area).

{% include img-small.html url="/assets/images/css-box-model/css-box-model-ex.png"  alt="Image of the CSS box model diagram from the Chrome developer tools." %}


## Review Questions

 - Explain the CSS Box Model.
 - What is the difference between margin and padding?
 - Does the margin show the background-color of the property it is applied to?  Does the padding?
 - What options are available when configuring a border for an element?
 - How do you use margins to center block content?
