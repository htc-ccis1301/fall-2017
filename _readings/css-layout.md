---
title: "CSS for Page Layout"
summary: "Introduction to CSS properties to modify and control the layout of your web page."
---


# {{ page.title }}
{{page.morea_summary}}

__I will not cover these topic in depth here. Make sure to read the linked articles below.__

## CSS Display Property
The CSS `display` property can be used to control how an element is displayed.  To understand how the display property is used, it is first helpful to understand that HTML has 2 main types of content: Block and Inline.

Block content starts on a new line and stretches across all of its allowed space.  Inline content on the other hand continues the current line and takes as little space as allowed.  This difference is best illustrated by a `<div>` which has block display and a `<span>` which has inline display.

Here is an example that highlights a div and a span in grey:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="boBvvQ" height="280" tab="html"
%}


There are several very handy updates to the display property values for flex & grid layouts.  However, for now it is only important to understand the four older and more commonly used values of `inline`, `inline-block`, `block` and `none`.

Read the following articles on the display property, focusing on the values noted above:

- [Learn CSS Layout: the "display" property"](http://learnlayout.com/display.html)
- [Learn CSS Layout: inline-block"](http://learnlayout.com/inline-block.html)
- [Learn CSS Layout: inline-block"](http://learnlayout.com/inline-block-layout.html)

This property is also covered in the CSS Almanac:
- [CSS Almanac: dipslay](https://css-tricks.com/almanac/properties/d/display/)


## Additional CSS for positioning
There are two other key CSS properties used for positioning and page layout: `float` & `position`.

### Position
Read the following articles to better understand how the `position` property is used:
- [Learn CSS Layout: position](http://learnlayout.com/position.html)
- [Learn CSS Layout: position example](http://learnlayout.com/position-example.html)

This property is also covered in the CSS Almanac:
- [CSS Almanac: position](https://css-tricks.com/almanac/properties/p/position/)

### Float & Clear
Read the following articles to better understand how the `float` and related properties are used:
- [Learn CSS Layout: float](http://learnlayout.com/float.html)
- [Learn CSS Layout: clear](http://learnlayout.com/clear.html)
- [Learn CSS Layout: clearfix](http://learnlayout.com/clearfix.html)
- [Learn CSS Layout: float layout example](http://learnlayout.com/float-layout.html)

This is also covered *very* thoroughly in the CSS Almanac:
- [CSS Almanac: float](https://css-tricks.com/almanac/properties/f/float/)
