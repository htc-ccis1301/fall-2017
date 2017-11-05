---
title: "Ms B's Veggies - Part 1"
summary: "Practice using the Bootstrap framework to build a basic single-page web site."
---

# {{ page.title }}
To learn how to use Bootstrap, we'll make a simple website together to get a feel for how everything works.  We'll build a simple site for Ms. B and Benji, some local heirloom gardeners.  

We'll be overriding some of the default Bootstrap styles to customize the look a bit.  It'll look like this when it is all finished.
{% include img-small.html
  url="/assets/images/bs-veggies/finished.png"  
  alt="Screenshot of the completed Ms B's Veggies site." %}

## Prerequisites
This exercise requires an understanding of the Bootstrap framework which you should have after completing *all* the reading for this module.

## GitHub
The GitHub repository for this assignment is [bs-veggies-bootstrap](https://classroom.github.com/a/YqaNAUDJ).

## Instructions

### Setup Bootstrap
Update the index.html page inside the project folder with the starter [Bootstrap template](https://getbootstrap.com/docs/4.0/getting-started/introduction/#starter-template).

Next, we'll customize the site for our new customer, Ms. B and her veggie stand.

1. Change the title to "Ms. B's Veggies".

2. Open the page and check the Console in the Browser Developer Tools to make sure that there are no errors getting the files from the CDN.  It should look like this:  
{% include img-medium.html url="/assets/images/bs-veggies/template.png"
    alt="Screenshot of Bootstrap template with Ms B's Veggies title." %}

Make sure that you didn't miss the updating the title (shown on the browser tab) and if the font seems different, you may not be getting the Bootstrap CSS files.  Check the Console in the Developer Tools for errors or missing files. You will need to be using Bracket's Live Preview feature to avoid security errors getting the CDN files.

### Add the Main Bootstrap Container
Add a `main` element to hold our page contents (the h1 for "Hello World"). We will set it up as our required Bootstrap container so that we can layout it's contents later using a grid.  Use the fixed width container (use the `container` class), so that we can center the container over that cool tartan background.  

Once the container is added, you should notice that there is now some padding and "Hello World!" is no longer squished along the left side of the browser display.

### Add the Footer
We will also add a fixed footer to the page.  Add a `<footer>` tag below the main element, just before the `<script>` tags.  Apply the `container-fluid` class to the footer so that it will span the full page width.  Add footer text to indicate that this site is copyright this year by Ms. B's Veggies.

Use the [Typography: Alignment](https://getbootstrap.com/docs/4.0/content/typography/#alignment) classes to center the content.

The page should now look like this:
{% include img-medium.html url="/assets/images/bs-veggies/main-footer-update.png"
    alt="Screenshot of Bootstrap template updated with main & footer." %}


### Main Content - Grid Layout
We'll use the Bootstrap Grid to make a responsive page layout for Ms. B and Benji.  This content will be structured into two rows. One for the featured veggies and their pictures, and a second for some general *about* information.

#### Row 1
Begin by removing the "Hello World" text from the `main` element and adding `div` elements to setup a row with 3-columns. Apply the appropriate styles to the columns so that:

- on mobile displays the first column will span the full width (12 columns), while the other two columns containing the pictures should sit side by side at 50% width (or 6 columns each).
- on tablets & desktops, the columns should display in a single row, with spacing of 50% - 25% - 25% (or 6-3-3 column widths).

##### First column content
The first column will contain the following information on the featured veggies.  Make the heading an `h2` and put the veggies in an unordered list.  

<blockquote>
Featured This Week
  <ul style="list-style-type: none;">
        <li>Jenny Lind Melon</li>
        <li>Yellow Pear Tomatoes</li>
        <li>Mortgage Lifter Tomatoes</li>
        <li>Henderson's Black Valentine Beans</li>
        <li>Chioggia Beet</li>
        <li>Fairytale Eggplant</li>
  </ul>
</blockquote>

Use the [Typography: Alignment](https://getbootstrap.com/docs/4.0/content/typography/#alignment) classes to center the content, and use the [List](https://getbootstrap.com/docs/4.0/content/typography/#lists) classes to remove the default list marker and margin.

##### Image columns
The next two columns should contain the pictures, one for Ms. B and the other for Benji.  You'll find image files for each of them in the images folder.  Add Bootstrap styles to the images to make the images responsive, with rounded corners.

Information on the making images responsive is found in the [Images](https://getbootstrap.com/docs/4.0/content/images/) documentation, while the rounded corner is found in [Utilities: Borders](https://getbootstrap.com/docs/4.0/utilities/borders/).

The site should now look like this:
<div class="row">
<div class="col-md-8">
<h5>Desktop</h5>
{% include img-responsive.html
    url="/assets/images/bs-veggies/row1-desktop.png"
    alt="Updated first row on desktop"
%}
</div><div class="col-md-4">
<h5>Mobile</h5>
{% include img-responsive.html
    url="/assets/images/bs-veggies/row1-mobile.png"
    alt="Updated first row on mobile"
%}
</div></div>

#### Responsive Reordering
They would like their pictures to surround the information on the featured vegetables of the week when shown on a wide-display. However when viewed on a mobile device, the features for  the week should be displayed first. To do this, we can alter the display order using [Bootstrap Grid: Column Reordering](https://getbootstrap.com/docs/4.0/layout/grid/#reordering).  

Adjust the styles so that:
- on a mobile sized devices, you see the featured veggies, followed by Ms. B and Benji underneath but side-by-side.
- on a desktop device, you see Ms. B on the left, the featured veggies in the middle, and Benji on the right.

With the reordering applied, the site should now look like this:
<div class="row">
<div class="col-md-8">
<h5>Desktop</h5>
{% include img-responsive.html
    url="/assets/images/bs-veggies/row1-reordered-desktop.png"
    alt="Reordered first row on desktop"
%}
</div><div class="col-md-4">
<h5>Mobile</h5>
{% include img-responsive.html
    url="/assets/images/bs-veggies/row1-mobile.png"
    alt="Updated first row on mobile"
%}
</div></div>

#### Row 2
Add a second row with a single full-width column to contain the following text:
<blockquote>
Ms. B's Veggies is a run by Ms. B, a local gardener and her trusty dog Benji. They've taken to the web to spread the word about their locally grown premium produce. Please show your support by stopping by to visit their vegetable stand.
</blockquote>

The site should now look as follows for the different display widths.
With the reordering applied, the site should now look like this:
<div class="row">
<div class="col-md-8">
<h5>Desktop</h5>
{% include img-responsive.html
    url="/assets/images/bs-veggies/row2-desktop.png"
    alt="Updated with 2nd row on desktop"
%}
</div><div class="col-md-4">
<h5>Mobile</h5>
{% include img-responsive.html
    url="/assets/images/bs-veggies/row2-mobile.png"
    alt="Updated with 2nd row on mobile"
%}
</div></div>

### Add the Jumbotron
We're going to add a Jumbotron to make an eye-catching display for Ms B.  Add a [Jumbotron](https://getbootstrap.com/docs/4.0/components/jumbotron/) inside our `main` Bootstrap container, before the grid rows we added above. It should contain the heading "Ms B's Heirloom Vegetables Fresh to your table" with the following text:
<blockquote>
Every Friday from noon - 3PM at:
<br>123 Garden Ave
<br>St. Paul, MN 55123
</blockquote>

Use a `<h1>` for the entire heading, but add the `small` tag with the `text-muted` class around the "Fresh to your table" sub-text. Add a `br` before the sub-text to break the line nicely.  The remaining text can just be a paragraph with line breaks added.

Your site should now look like this:
{% include img-small.html
  url="/assets/images/bs-veggies/jumbotron.png"
  alt="Screenshot of Ms B's Veggies with Jumbotron." %}


### Add the Navbar
Refer back to the [Navbar](https://getbootstrap.com/docs/4.0/components/navbar/) documentation to add a __fixed__ Navbar that looks like this:
{% include img-small.html
  url="/assets/images/bs-veggies/navbar.png"  
  alt="Screenshot of the Navbar for Ms B's Veggies." %}

The *brand* link, "Ms. B's Veggies" should link to this Home page.  The other links can just go to "#" for the moment.  We may add more pages later, but we will not add them for this assignment.  

Note that the `navbar` class should be placed on a `<nav>` tag and should be positioned before the `main` element that we added earlier.

Two important things to test:

1. Check that the Navbar remains positioned at the top while you scroll.
2. Verify the navbar collapses only for mobile (xs and sm) display. You can control the collapse functionality with [Navbar: Responsive Behaviors](https://getbootstrap.com/docs/4.0/components/navbar/#responsive-behaviors).

The top of the Jumbotron is hidden under our fixed header.  We will need to add some padding-top to the body element to fix this. Create a new stylesheet and link to in in the home page header. The navbar is about 70px high, so we will add 70px of padding to the top of the `body` element.

After adding the padding, the page should now look like this:
{% include img-small.html
  url="/assets/images/bs-veggies/body-padding.png"  
  alt="Screenshot of the Navbar for Ms B's Veggies with padding-top on the body." %}

This leaves us with a somewhat boring, default styled Bootstrap website.  We will continue adding custom styles in Part 2 of this assignment to tailor the page for Ms B.
