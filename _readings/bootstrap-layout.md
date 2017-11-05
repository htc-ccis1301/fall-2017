---
title: "Bootstrap Page Layout"
summary: "An introduction to some of the CSS provided in the Bootstrap framework."
---

# {{ page.title }}
Most of what Bootstrap provides is a responsive, mobile first CSS framework to use when building your site.  We'll begin by looking at the classes for page layout.

## Layout
In [Layout](http://getbootstrap.com/docs/4.0/layout/) you will find responsive CSS classes to help with the responsive design and layout of your page. These Bootstrap classes replace the use of media queries for most of your web site layout needs.  

### Containers & Breakpoints
The [Overview](https://getbootstrap.com/docs/4.0/layout/overview/) page explains the two different types of containers: the centered, fixed-width `container` and the full width `container-fluid`. Further down the page, the responsive breakpoints are explained.  You will see the sizes referred to in the [Grid](https://getbootstrap.com/docs/4.0/layout/grid/) documentation, so it is important to understand what Bootstrap uses these sizes to represent:

- `xs` & `sm` (phone)
- `md` (tablet)
- `lg` (desktop)
- `xl` (larger, widescreen desktop)

### Responsive Grid
The [Grid](https://getbootstrap.com/docs/4.0/layout/grid/) is the foundation of the Bootstrap layout.  It is extremely important that you understand how the grid classes are used and applied to create different page layouts. Read through the documentation and make a practice page to try out some different layouts.

See if you can create pages that look like the following examples.  You can use the starter HTML files in the [Bootstrap Layout Practice](https://classroom.github.com/a/kMnI2bBa) GitHub repository. There is no need to add any HTML to the files, just add style classes to the existing HTML elements.

#### Fixed width with sidebar (fixed-width-sidebar.html):
<div class="row">
<div class="col-md-8">
<h5>Desktop</h5>
{% include img-responsive.html
    url="/assets/images/bootstrap/fixed-w-sidebar-lgdisplay.png"
    alt="Fixed width with sidebar on desktop"
%}
</div><div class="col-md-4">
<h5>Mobile</h5>
{% include img-responsive.html
    url="/assets/images/bootstrap/fixed-w-sidebar-smdisplay.png"
    alt="Fixed width with sidebar on mobile"
%}
</div></div>

#### Full width with sidebar (full-width-sidebar.html):
<div class="row">
<div class="col-md-8">
<h5>Desktop</h5>
{% include img-responsive.html
    url="/assets/images/bootstrap/full-w-sidebar-lgdisplay.png"
    alt="Full width with sidebar on desktop"
%}
</div><div class="col-md-4">
<h5>Mobile</h5>
{% include img-responsive.html
    url="/assets/images/bootstrap/full-w-sidebar-smdisplay.png"
    alt="Full width with sidebar on mobile"
%}
</div></div>

#### Full width with 2 equal columns (full-width-two-column.html):
<div class="row">
<div class="col-md-8">
<h5>Desktop</h5>
{% include img-responsive.html
    url="/assets/images/bootstrap/full-2eq-col-lgdisplay.png"
    alt="Full width with 2 equal columns on desktop"
%}
</div><div class="col-md-4">
<h5>Mobile</h5>
{% include img-responsive.html
    url="/assets/images/bootstrap/full-2eq-col-smdisplay.png"
    alt="Full width with 2 equal columns on mobile"
%}
</div></div>
