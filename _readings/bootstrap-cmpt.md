---
title: "Bootstrap CSS & Components"
summary: "An introduction to the content focused CSS and user interface (UI) components provided in the Bootstrap framework."
---

# {{ page.title }}

## Content
The [Content](http://getbootstrap.com/docs/4.0/content/).  Each section page introduces the main CSS classes. Read through the Reboot section for an introduction to the Reboot styles. These styles are applied to specific HTML tags, so you don't need to do anything but include the Bootstrap CSS for the styles to be applied to those elements.

### Typography & Code
Bootstrap includes many CSS style classes that are pre-built to apply a specific look to an element.  The [Typography](https://getbootstrap.com/docs/4.0/content/typography/) classes are focused on the presentation of text content. The [Code](https://getbootstrap.com/docs/4.0/content/code/) classes are formatting for technical content.

### Images & Figures
The [Images](https://getbootstrap.com/docs/4.0/content/images/) and [Figure](https://getbootstrap.com/docs/4.0/content/figures/) classes are used for styling images and figures (images with text). The most common of these is the `img-fluid` class. Applying the `img-fluid` class will auto adjust your image sizes to fit in responsive containers, such as the Bootstrap Grid.  There are also classes to round the corners or put the image in a circle.


### Tables
Bootstrap also provides CSS classes to add a default style to [tables](https://getbootstrap.com/docs/4.0/content/tables/).  Unlike the Reboot styles applied to elements by default, you may choose which (if any) style classes to your HTML tables. For example, just adding the `table` style class to the table tag gives you a basic table with a border separating the rows. Explore the various examples shown on the page to see the many possibilities for Bootstrap table styling.

### Utilities & Extensions
Bootstrap includes many other helpful [utilities](https://getbootstrap.com/docs/4.0/utilities/borders/) classes and [extensions](https://getbootstrap.com/docs/4.0/extend/icons/) to aid in the creation of a nice user interface for your page.  Please review the docs for details and examples.

There are many other [Components](https://getbootstrap.com/docs/4.0/components/) classes included in the Bootstrap library. (Look down the list on the menu on the left side.) We'll discuss a few below. It's worth taking a look through the entire list just to be familiar with what they already have built for you.

For example, when I first learned Bootstrap, I didn't have any need of multi-colored alert boxes, but since I've started making websites for my classes, calling out common errors, warnings and info tips in different colors has been quite handy. While I didn't remember the actual CSS class names, I recalled seeing them in the Bootstrap docs years later and looked them up.  Because I recalled seeing these, I avoided writing my own CSS to do the same thing.

{% include alert.html type="warning"
   content="Note that some of these components require JavaScript, while others do not.  If you are not using any of the JS components, including jQuery and the other `script` tags is not required. However if you use any of these JS components, you must include the `script` tags from the template for them to work correctly."
%}

## UI Components

### Navigation
There are several different options for setting up and organizing a site's links and navigation.  Bootstrap supports both `nav` styling as well as a JavaScript enabled Navbar.

{% include alert.html type="tip"
   content="When looking at the examples in the docs, remember to resize your display to view their responsive behavior."
%}

#### Nav
The [nav](https://getbootstrap.com/docs/4.0/components/navs/) classes allow you to improve the look of basic `nav` links.  There are several options for horizontal & vertical styles, and even a tabbed display.  If JavaScript is included, dropdown menus can also be added.


#### Navbar
Bootstrap also provides a full [navbar](https://getbootstrap.com/docs/4.0/components/navbar/) that sits along the top of the web page. This component is a bit more complex than the simple nav styling classes shown above. Read through the docs carefully to understand fully how this component works. It is helpful to build and experiment with an example while learning so that you can make changes and see the results.


### Scrollspy
The [Scrollspy](https://getbootstrap.com/docs/4.0/components/scrollspy/) component is used to keep the nav component in sync with the position of the content when scrolling down a page in the browser.  We've used in-page links in the past to navigate to a section further down the page. The `scrollspy` component uses the nav links and anchors to highlight the nav item corresponding to the location on the page we have scrolled or linked down to. Read the docs carefully to see how it is set up.

### Jumbotron
The [Jumbotron](https://getbootstrap.com/docs/4.0/components/jumbotron/) component is intended for displaying a large marketing message, often with a nice big background image, to catch the attention of visitors right away.  It's pretty straightforward component, but it's appearance will change based on whether it is a standard `jumbotron` or a `jumbotron-fluid`.  

### Carousel
The [Carousel](https://getbootstrap.com/docs/4.0/components/carousel/) component is another option for displaying a prominent, eye catching marketing message.  It is similar to the Jumbotron, but it allows you to rotate through a series of different images or messages. There are a variety of options available for customizing the display and functionality.  Read the docs for more details. This component also requires JavaScript in order to handle the rotation of the images.

### Cards
The [Card](https://getbootstrap.com/docs/4.0/components/card/) component is a way to format and display a series of content items that have a similar structure. For example, the Module page or a Module "home" page from this course website might be created as cards, with each "block" of content representing a card. (Actually this site is styled with Bootstrap 3, and they are `panels` the predecessor of the Bootstrap 4 `card`.)
