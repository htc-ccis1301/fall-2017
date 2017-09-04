---
title: "Colors in CSS"
summary: "Information on how colors are specified and applied using CSS."
---

# {{ page.title }}
{{ page.summary }}

## Colors with CSS
Colors in CSS can be specified in a few different ways.  In the first examples above, special color names were used. However there are only 140 [Named CSS Colors](http://htmlcolorcodes.com/color-names/) for the web, so that is pretty limiting. Fortunately we now have access to an almost limitless amount of color through the use of hex color codes and RGB color specifications.  

{% include youtube-16x9.html id="JBRZ3KBfOk8"
    caption="Thanks [Webflow](https://www.youtube.com/channel/UCELSb-IYi_d5rYFOxWeOz5g) for sharing this video."
%}

## Hex Color Codes
Historically (before CSS3) the most common way to express a color in CSS was by using a hexadecimal value or __hex-code__ to represent the color. In a hex-code, the amount of red, green, and blue used to make the color is specified in [hexadecimal]() notation.  

Hexadecimal is a number system that uses a base of 16 instead of 10, much like *binary* uses a base of two. In our decimal (base 10) number system we use the numbers 0-9. In binary (base 2) we use 0 or 1. Hexadecimal is base 16 and since we do not have 16 numeric digits available it uses 0-9 plus the letters A-F to get 16 possible values.

Hexadecimal color codes use two hexadecimal characters (0-9, A-F), or one byte, to represent each color.  There is one byte (or two characters) for red, two more for green, and two more for blue. This gives us codes that are 6 characters in length.

![Hex Color Code]({{"/assets/images/basic-css/hex-color-code.png" | prepend: site.baseurl}})

Lower numbers represent low color intensity, producing darker colors. For example, `#000000` is black. Lighter colors have higher numbers to represent higher intensity. White is maximum intensity or `#FFFFFF`. By varrying the intensity of each color equally, we get shades of grey.

<table class="table">
  <thead>
    <tr>
      <th>Hex Code</th>
      <th>Color Sample</th>
      <th>Color Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">#000000</th>
      <td><div style="background-color:#000; width:100px; height:30px"></div></td>
      <td>black</td>
    </tr>
    <tr>
      <th scope="row">#303030</th>
      <td><div style="background-color:#303030; width:100px; height:30px"></div></td>
      <td>a very dark grey</td>
    </tr>
    <tr>
      <th scope="row">#555555</th>
      <td><div style="background-color:#555; width:100px; height:30px"></div></td>
      <td>a dark grey</td>
    </tr>
    <tr>
      <th scope="row">#808080</th>
      <td><div style="background-color:#808080; width:100px; height:30px"></div></td>
      <td>(medium) grey</td>
    </tr>
    <tr>
      <th scope="row">#AAAAAA</th>
      <td><div style="background-color:#AAA; width:100px; height:30px"></div></td>
      <td>a lighter grey</td>
    </tr>
    <tr>
      <th scope="row">#DDDDDD</th>
      <td><div style="background-color:#DDDDDD; width:100px; height:30px"></div></td>
      <td>silver grey</td>
    </tr>
    <tr>
      <th scope="row">#FFFFFF</th>
      <td><div style="background-color:#FFF; width:100px; height:30px; border: 1px #DDD solid"></div></td>
      <td>white</td>
    </tr>
  </tbody>
</table>

Of course we are not limited to shades of grey. By changing the amount of the red, green, & blue component colors, we are able to get an amazing amount of variation.

<table class="table">
  <thead>
    <tr>
      <th>Hex Code</th>
      <th>Color Sample</th>
      <th>Color Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">#FF0000</th>
      <td><div style="background-color:#F00; color:#FFF; width:100px; height:30px"></div></td>
      <td>red<br> (no green or blue)</td>
    </tr>
    <tr>
      <th scope="row">#00FF00</th>
      <td><div style="background-color:#0F0; color:#000; width:100px; height:30px"></div></td>
      <td>green<br> (no red or blue)</td>
    </tr>
    <tr>
      <th scope="row">#0000FF</th>
      <td><div style="background-color:#00F; color:#FFF; width:100px; height:30px"></div></td>
      <td>blue<br> (no red or green)</td>
    </tr>
    <tr>
      <th scope="row">#FFFF00</th>
      <td><div style="background-color:#FF0; color:#000; width:100px; height:30px"></div></td>
      <td>yellow<br> (red and green, no blue)</td>
    </tr>
    <tr>
      <th scope="row">#800080</th>
      <td><div style="background-color:#800080; color:#FFF; width:100px; height:30px"></div></td>
      <td>purple<br> (red and blue, no green)</td>
    </tr>
  </tbody>
</table>

By blending the amounts of each color more subtly, we get even more shade variations.

<table class="table">
  <thead>
    <tr>
      <th>Hex Code</th>
      <th>Color Sample</th>
      <th>Color Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">#FFE4E1</th>
      <td><div style="background-color:#FFE4E1; width:100px; height:30px"></div></td>
      <td>a light hint of pink</td>
    </tr>
    <tr>
      <th scope="row">#FFC0C8</th>
      <td><div style="background-color:#FFC0C8; width:100px; height:30px"></div></td>
      <td>cotton candy pink</td>
    </tr>
    <tr>
      <th scope="row">#F08080</th>
      <td><div style="background-color:#F08080; width:100px; height:30px"></div></td>
      <td>rose pink</td>
    </tr>
    <tr>
      <th scope="row">#FA8072</th>
      <td><div style="background-color:#FA8072; width:100px; height:30px"></div></td>
      <td>salmon pink</td>
    </tr>
    <tr>
      <th scope="row">#E9967A</th>
      <td><div style="background-color:#E9967A; width:100px; height:30px"></div></td>
      <td>neutral pink</td>
    </tr>
    <tr>
      <th scope="row">#FF69B4</th>
      <td><div style="background-color:#FF69B4; width:100px; height:30px"></div></td>
      <td>dark pink</td>
    </tr>
    <tr>
      <th scope="row">#FF1493</th>
      <td><div style="background-color:#FF1493; width:100px; height:30px"></div></td>
      <td>hot pink</td>
    </tr>
  </tbody>
</table>

### Example Page
Here is an example of a page with some CSS applied to add color using hex codes:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="qXgePN" height="400" tab="css"
%}

### Short Hex Codes
In the example above, the hex-code `#DDD` appears. This is a shortened form of `#DDDDDD`. When the two characters that make up a byte of the hex-code is the same, the code may optionally be shortened to 3 characters. You can only do this when both characters in a byte are identical, so `#A0A0A0` __cannot__ be shortened to `#A0A` as that is the color `#AA00AA`.

## RGB Colors
Colors in CSS can also be expressed using an RGB color code. This behaves very similar to the hex-code color representation in that the amounts of red, green, and blue are specified separately, but with the RGB codes, we use a decimal number from 0-255 instead of hexadecimal values for each color value.

We can express the same colors using either hex-codes or RGB:

<table class="table">
  <thead>
    <tr>
      <th>Hex Code</th>
      <th>RGB Color</th>
      <th>Color Sample</th>
      <th>Color Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">#000000</th>
        <th scope="row">rgb(0,0,0)</th>
      <td><div style="background-color:rgb(0,0,0); width:100px; height:30px"></div></td>
      <td>black</td>
    </tr>
    <tr>
      <th scope="row">#303030</th>
      <th scope="row">rgb(40,40,40)</th>
      <td><div style="background-color:rgb(40,40,40); width:100px; height:30px"></div></td>
      <td>a very dark grey</td>
    </tr>
    <tr>
      <th scope="row">#555555</th>
        <th scope="row">rgb(85,85,85)</th>
      <td><div style="background-color:rgb(85,85,85); width:100px; height:30px"></div></td>
      <td>a dark grey</td>
    </tr>
    <tr>
      <th scope="row">#808080</th>
        <th scope="row">rgb(128,128,128)</th>
      <td><div style="background-color:rgb(128,128,128); width:100px; height:30px"></div></td>
      <td>(medium) grey</td>
    </tr>
    <tr>
      <th scope="row">#AAAAAA</th>
        <th scope="row">rgb(170,170,170)</th>
      <td><div style="background-color:rgb(170,170,170); width:100px; height:30px"></div></td>
      <td>a lighter grey</td>
    </tr>
    <tr>
      <th scope="row">#DDDDDD</th>
        <th scope="row">rgb(221,221,221)</th>
      <td><div style="background-color:rgb(221,221,221); width:100px; height:30px"></div></td>
      <td>silver grey</td>
    </tr>
    <tr>
      <th scope="row">#FFFFFF</th>
      <th scope="row">rgb(255,255,255)</th>
      <td><div style="background-color:rgb(255,255,255); width:100px; height:30px; border: 1px #DDD solid"></div></td>
      <td>white</td>
    </tr>
    <tr>
      <th scope="row">#FF0000</th>
      <th scope="row">rgb(255,0,0)</th>
      <td><div style="background-color:rgb(255,0,0); width:100px; height:30px"></div></td>
      <td>red<br> (no green or blue)</td>
    </tr>
    <tr>
      <th scope="row">#00FF00</th>
      <th scope="row">rgb(0,255,0)</th>
      <td><div style="background-color:rgb(0,255,0); width:100px; height:30px"></div></td>
      <td>green<br> (no red or blue)</td>
    </tr>
    <tr>
      <th scope="row">#0000FF</th>
      <th scope="row">rgb(0,0,255)</th>
      <td><div style="background-color:rgb(0,0,255); width:100px; height:30px"></div></td>
      <td>blue<br> (no red or green)</td>
    </tr>
    <tr>
      <th scope="row">#FFFF00</th>
      <th scope="row">rgb(255,255,0)</th>
      <td><div style="background-color:rgb(255,255,0); width:100px; height:30px"></div></td>
      <td>yellow<br> (red and green, no blue)</td>
    </tr>
    <tr>
      <th scope="row">#800080</th>
      <th scope="row">rgb(128, 0, 128)</th>
      <td><div style="background-color:rgb(128, 0, 128); width:100px; height:30px"></div></td>
      <td>purple<br> (red and blue, no green)</td>
    </tr>
    <tr>
      <th scope="row">#FFE4E1</th>
      <th scope="row">rgb(255, 228, 225)</th>
      <td><div style="background-color:rgb(255, 228, 225); width:100px; height:30px"></div></td>
      <td>a light hint of pink</td>
    </tr>
    <tr>
      <th scope="row">#FFC0C8</th>
      <th scope="row">rgb(255, 192, 200)</th>
      <td><div style="background-color:rgb(255, 192, 200); width:100px; height:30px"></div></td>
      <td>cotton candy pink</td>
    </tr>
    <tr>
      <th scope="row">#F08080</th>
      <th scope="row">rgb(240, 128, 128)</th>
      <td><div style="background-color:rgb(240, 128, 128); width:100px; height:30px"></div></td>
      <td>rose pink</td>
    </tr>
    <tr>
      <th scope="row">#FA8072</th>
      <th scope="row">rgb(250, 128, 114)</th>
      <td><div style="background-color:rgb(250, 128, 114); width:100px; height:30px"></div></td>
      <td>salmon pink</td>
    </tr>
    <tr>
      <th scope="row">#E9967A</th>
      <th scope="row">rgb(233, 150, 122)</th>
      <td><div style="background-color:rgb(233, 150, 122); width:100px; height:30px"></div></td>
      <td>neutral pink</td>
    </tr>
    <tr>
      <th scope="row">#FF69B4</th>
      <th scope="row">rgb(255, 105, 180)</th>
      <td><div style="background-color:rgb(255, 105, 180); width:100px; height:30px"></div></td>
      <td>dark pink</td>
    </tr>
    <tr>
      <th scope="row">#FF1493</th>
      <th scope="row">rgb(255, 20, 147)</th>
      <td><div style="background-color:rgb(255, 20, 147); width:100px; height:30px"></div></td>
      <td>hot pink</td>
    </tr>
  </tbody>
</table>

### Transparency
CSS3 provides an extension to the RGB color coding to allow for a transparency to be added. This allows the color to have an `alpha` value ranging from 0 (transparent) to 1 (opaque). These colors are called __rgba colors__ to indicate the __alpha__, or transparency, value is added.

<table class="table">
  <thead>
    <tr>
      <th>RGBA Color</th>
      <th>Color Sample</th>
      <th>Color Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">rgba(0,0,0,1)</th>
      <td><div style="background-color:rgba(0,0,0,1); width:100px; height:30px"></div></td>
      <td>black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.8)</th>
      <td><div style="background-color:rgba(0,0,0,0.8); width:100px; height:30px"></div></td>
      <td>80% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.6)</th>
      <td><div style="background-color:rgba(0,0,0,0.6); width:100px; height:30px"></div></td>
      <td>60% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.4)</th>
      <td><div style="background-color:rgba(0,0,0,0.4); width:100px; height:30px"></div></td>
      <td>40% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.2)</th>
      <td><div style="background-color:rgba(0,0,0,0.2); width:100px; height:30px"></div></td>
      <td>20% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0)</th>
      <td><div style="background-color:rgba(0,0,0,0); width:100px; height:30px; border: 1px #DDD solid"></div></td>
      <td>fully transparent (invisible) black</td>
    </tr>
  </tbody>
</table>

In the table above, the color appears to just lighten from black into grey and finally into white as it becomes more and more transparent. However that is only because the background-color of the table above is white.  

Notice how the same set of black colors appears differently against a tan background.

<div style="background-color:#CD853F;">
<table class="table">
  <thead>
    <tr>
      <th>RGBA Color</th>
      <th>Color Sample</th>
      <th>Color Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">rgba(0,0,0,1)</th>
      <td><div style="background-color:rgba(0,0,0,1); width:100px; height:30px"></div></td>
      <td>black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.8)</th>
      <td><div style="background-color:rgba(0,0,0,0.8); width:100px; height:30px"></div></td>
      <td>80% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.6)</th>
      <td><div style="background-color:rgba(0,0,0,0.6); width:100px; height:30px"></div></td>
      <td>60% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.4)</th>
      <td><div style="background-color:rgba(0,0,0,0.4); width:100px; height:30px"></div></td>
      <td>40% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0.2)</th>
      <td><div style="background-color:rgba(0,0,0,0.2); width:100px; height:30px"></div></td>
      <td>20% opaque black</td>
    </tr>
    <tr>
      <th scope="row">rgba(0,0,0,0)</th>
      <td><div style="background-color:rgba(0,0,0,0); width:100px; height:30px; border: 1px #DDD solid"></div></td>
      <td>fully transparent (invisible) black</td>
    </tr>
  </tbody>
</table>
</div>

The ability to layer multiple HTML elements that have different colors and transparency values applied through CSS allows web page designers to create some very interesting effects on the Web.

## Gradients
CSS3 also allows us to apply gradient colors to an element. Being able to configure gradients in CSS is awesome!  The radial gradient provides a nice spot-light effect that is pretty neat, while the linear gradient makes for a simple but interesting background.  

Often we will use a gradient background for the body, and place a solid white (or light-colored) content area over top of it.  That light, solid color makes it easier to read any text.  

When we use a gradient background, we should always specify a solid fall-back color for browsers that may not support CSS gradients.

### Linear Gradient
This example uses a linear gradient. Note there is a fall-back color specified using the `background-color` property and the gradient is setup using the `background-image` property. To avoid having the gradient repeat, the `background-repeat` property is also set.
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="zdbzZa" height="300" tab="css"
%}


### Radial Gradient
This next example uses a radial (or rounded) gradient. Again, note that a fall-back color is specified using the `background-color` property.
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="ayMwwR" height="300" tab="css"
%}

## Review Questions

 - Name three ways that colors can be specified in CSS.
 - How many characters are in a hex code?
 - What are valid values for each character in a hex code?
 - What conditions must be met for a hex code to be shortened?
 - What are valid values for each number in an rgb color code?
 - What is the hex code for the color black? What is the rgb code?
 - What is the hex code for the color white? What is the rgb code?
 - What does the "a" in rgba stand for? What is it used for?
 - What CSS property is used to make a background gradient?
 - Why should you provide a fall-back background-color when using a CSS gradient?
