---
title: "Ms B's Veggies - Part 2"
summary: "The continuation of Ms B's Veggies website build. In this part we will apply customizations to the page to make it look more unique."
---

# {{ page.title }}
In this part of the assignment, we will customize the CSS for Ms B's website to make the site look more unique.

Your site should now look like this:
{% include img-small.html
  url="/assets/images/bs-veggies/body-padding.png"  
  alt="Screenshot of the Navbar for Ms B's Veggies with padding-top on the body." %}

In this part, we'll add custom CSS so that it will look like this:
{% include img-small.html
  url="/assets/images/bs-veggies/finished.png"  
  alt="Screenshot of the completed Ms B's Veggies site." %}

## Prerequisites
This exercise requires an understanding of the Bootstrap framework which you should have after completing *all* the reading for this module.  It is also important that you have completed Part 1 of this exercise.

## GitHub
The GitHub repository for this assignment is [bs-veggies-bootstrap](https://classroom.github.com/a/YqaNAUDJ).

You do not need to accept the assignment or clone the repository again. Continue working with the files you had from part 1.

## Instructions

### Custom Stylesheet
Make sure that the custom stylesheet that you added is located *__after__* the Bootstrap stylesheet in your HTML file.  Order is important as we will want to customize (override) some of the default Bootstrap styles to get our final version of the site.

### Customize the Color Scheme
To begin, let's give Ms B's site a more friendly and homey look and feel.  Ms. B loves minty green and purple, so we've got a color scheme worked up just for her from the [Paletton](http://paletton.com/palette.php?uid=32S0u0kcglL4Zvw8Eq6eXhmkwen) website.  We'll use this and the fancy tartan background image (generated from the Paletton site) to transform this into a site even Benji will love.

Update the stylesheet to:

1. Add the tartan background image to the body, and set a fall back background-color of #A2C0A7.
2. Add css to style the `main` element with the background-color of #FBE7D4, and set padding of 25px to the top and bottom.
3. Add spacing below each `row` in our main content by adding bottom margin of 15px.
4. Adjust the color on the footer to be #CEAEBF and the background-color to #5E2241.
5. Add css to style the `.btn` class to have the background-color of #CEAEBF and the color of #5E2241.

We will also make a few style customizations in the HTML file, by adding or adjusting the Bootstrap styles applied:
1. Use the Bootstrap utility class to round the borders on the main element. (This is an HTML file change.)
2. Change the `navbar` to be `navbar-dark` and add an inline style to set the `background-color` to #5E2241.

Your site should now look like this:
{% include img-small.html
  url="/assets/images/bs-veggies/first-style-updates.png"  
  alt="Screenshot of after the above style updates." %}

### Customize the Jumbotron
Overall things look pretty good, but let's wrap up by updating that Jumbotron.  Add the following styles for the Jumbotron:

- set bottom padding to 25px
- set the text color to black
- add a drop shadow on the text using the color #FBE7D4, for sizing use 3px horizontal, 3px vertical, and 4px blur
- add the 'veggies-background' background image, have it cover the container and clip on the border
- change the color of the jumbotron `small` text to #1F5829
- change the font size on the jumbotron paragraphs to be 1.3em and make the text bold

In the HTML, center align the jumbotron text by applying the appropriate Bootstrap style class.


With the jumbotron updates, our final site should look like this:
In this part, we'll add custom CSS so that it will look like this:
{% include img-small.html
  url="/assets/images/bs-veggies/finished.png"  
  alt="Screenshot of the completed Ms B's Veggies site." %}


## Submit
Create a pull-request and submit the screenshot of it in the Assignment box on D2L.

You must also submit screenshots that show you have validated both the CSS & HTML file for this assignment and have no errors found.  Please ensure that you capture the validator URL and the validator output in each screenshot.
