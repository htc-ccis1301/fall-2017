---
title: "Page Layout & Design"
summary: "In this reading, we'll explore some more trendy page layouts with an introduction to responsive design."
---

# {{ page.title }}
{{ page.morea_summary }}

## Web Articles
Read the following articles from the web:

- [10 Rock Solid Website Layout Examples](https://designshack.net/articles/layouts/10-rock-solid-website-layout-examples/)
- [Responsive Design Examples](http://designmodo.com/responsive-design-examples/)

As you read through the first article, notice that they first illustrate the page layout using block wireframes so that you can see the pattern without distraction.  They will then show example pages that use this layout.  

For example the first layout they call "Three Boxes":

<div style="padding:10px">
  <div class="row">
    <div class="col-xs-12 col-md-6">
        <img class="img-responsive" src="{{ "/assets/images/design-layout/block-layout.png" | prepend:site.baseurl }}" alt="Wireframe three boxes layout.">
    </div>
    <div class="col-xs-12 col-md-6">
        <img class="img-responsive" src="{{ "/assets/images/design-layout/block-layout-applied.png" | prepend:site.baseurl }}" alt="Example site using three boxes layout.">
    </div>
  </div>
</div>

As you read through the article, practice matching the example sites back to the block wireframe designs.  This will help you learn to identify the structure that web sites you visit are built on.  You will be applying this technique later for one of your weekly exercises.

The second article discusses responsive design, a context-aware design that alters its layout based on the size of the device that it is viewed on.  We will learn more about how to make a responsive design in later modules. For now, however, focus on the page layouts that are shown.  Notice that instead of one layout, these sites have three.

For example, the main Designmodo site layout looks like this:

<div style="padding:10px">
  <div class="row">
    <div class="col-xs-12 col-md-8">
        <img class="img-responsive" src="{{ "/assets/images/design-layout/designmodo-full.png" | prepend:site.baseurl }}" alt="Full size designmodo site.">
    </div>
  </div>
</div>

But when viewing on a tablet or smart phone, the layout shifts:
<div style="padding:10px">
  <div class="row">
    <div class="col-xs-12 col-md-7">
        <img class="img-responsive" src="{{ "/assets/images/design-layout/designmodo-tablet.png" | prepend:site.baseurl }}" alt="Tablet size designmodo site.">
    </div>
    <div class="col-xs-12 col-md-5">
        <img class="img-responsive" src="{{ "/assets/images/design-layout/designmodo-phone.png" | prepend:site.baseurl }}" alt="Phone size designmodo site.">
    </div>
  </div>
</div>

Can you see the differences in the layouts?  It might help to go to the [Designmodo site](http://designmodo.com/) and alter the width of your browser window to see the layout shift.

- The desktop layout includes spacing along the sides to center the content and prevent it from stretching too wide.
- The tablet layout removes the empty spaces along the sides, and the top product ad bar above the navigation.  
- The mobile phone layout removes the right sidebar and further minimizes the navigation.  However you should note that the content from that right sidebar was not removed, it was just shifted down to the bottom of the page, so it is under all the main content that was on the left.

### 60 30 10 Rule
A standard of web design, which originates in interior design, is the 60-30-10 rule.  It can be applied both to the spacing of your web content and your use of colors.

For spacing, you might aim for:
<div style="padding:10px">
  <div class="row">
    <div class="col-xs-12 col-md-6">
        <p>Desktop</p>
        <ul>
          <li>60% negative (empty) space</li>
          <li>30% content</li>
          <li>10% call-to-action (or special) items</li>
        </ul>
    </div>
    <div class="col-xs-12 col-md-6">
        <p>Mobile</p>
        <ul>
          <li>60% content</li>
          <li>30% negative (empty) space</li>
          <li>10% call-to-action (or special) items</li>
        </ul>
    </div>
  </div>
</div>

This is just a general guideline, but it helps to give a balanced and cohesive look to your site while preventing a crowded look and feel.


### Golden Ratio
Another standard of design is the golden ratio.  The golden ratio is a mathematical ratio found throughout nature.  It is closely related to the Fibonacci Sequence and is approximately a 1:1.61 ratio.

Note the Fibonacci Sequence is 0, 1, 1, 2, 3, 5, 8, 13, etc.  Each number is the sum of the two prior numbers.  Note how the rectangle below is built using this sequence.

{% include img-small.html url="/assets/images/design-layout/golden-ratio.png" alt="Image of golden rectangle."
%}

Many websites will use this to size the different blocks of their site content.

{% include youtube-16x9.html id="kkGeOWYOFoA" caption="A movie inspired on numbers, geometry and nature, by Cristóbal Vila, [Eterea Studios](www.etereaestudios.com)"
%}

## Wrap-up
The next module will focus more on web design and responsive layouts.  While the intent of these lessons isn't to train you to be a web designer, you do need to have an eye for page structure and layout in order to build one. In addition, a basic understanding of good design can come in handy when you need to make a nice looking page and there isn't a full-time designer on staff.
