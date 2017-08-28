---
title: "HTML Validation"
summary: "An introduction to using the W3C HTML Validator to validate your HTML files, and some tips on resolving validation errors."
---

# {{ page.title }}
{{page.morea_summary}}

## W3C HTML Validator
We will use the [W3C HTML Validator](https://validator.w3.org/) to validate all of our HTML pages for correctness.

The validator cannot check that the semantics of our page are correct, that is it cannot check that we have chosen the correct tags to markup certain content, however it can ensure that the tags we have chosen are used correctly as defined by the HTML5 specification. When we use valid HTML that meets the specification we are *more likely* (but not absolutely certain) to have our pages displayed consistently across different browsers.

### Browser Support
Why can't we be certain that our HTML will display consistently even if it meets the W3C specification perfectly?  Because the Internet is open, and it is up to the browser developers to ensure that the browsers they make correctly support the most current HTML specification. Unfortunately the various browser developers may not be in conformance with or up to date with the latest specification, even when it is now years old.

The website [Can-I-Use](https://caniuse.com/) is used by many web developers to get an understanding of browser demographics (which browsers are in use and by how many people) and what parts of the HTML & CSS specifications are supported by the various browsers and versions. It can be a complex issue, balancing the desire to write to the latest spec (specification) while still needing to support older browsers that are still in use by significant percentages of the population.

We will not be overly concerned with browser compatibility and support in this course, though we will learn a few techniques that should be used consistently to help ensure our pages display appropriately in older and non-conforming HTML5 browsers.


## Validation Walkthrough
Let's walk through the steps you would go through to validate a web page using the [W3C HTML Validator](https://validator.w3.org/).

First go to the [W3C HTML Validator](https://validator.w3.org/) on the web. You'll see that it looks something like this:

{% include img-medium.html url="/assets/images/intro-valid-html/w3c-html-validator.png"
    alt="Image of the W3C validator website, highlighting the tabs for different types of input."
%}

Note the tabs that allow different types of input.  

### Validate by URI
The first tab "Validate by URI" is used to validate an HTML page published on the Internet.

Let's use this to validate a sample HTML page. We'll use my HTML only [Ice-Cream is Awesome!](https://htc-ccis1301.github.io/demo-ice-cream/html-only.html) page.  

First, open the W3C Validator and make sure that you are on the Validate by URI tab.

Next, copy this URL: https://htc-ccis1301.github.io/demo-ice-cream/html-only.html and paste it into the Address field on the form.  Then click the Check button.

{% include img-medium.html url="/assets/images/intro-valid-html/validate-by-uri.png"
    alt="Image of Validate by URI tab showing the above URL pasted in & the Check button to click in order to validate."
%}

After clicking "Check", the validation results will display showing that this page is valid.  Note that the message displays in green for "good". Warnings will be highlighted in yellow/orange and if there are errors it will be red.  The status is also clearly indicated by the message text, but the color can be a quick cue if you are able to see and distinguish it.

{% include img-medium.html url="/assets/images/intro-valid-html/valid-output.png"
    alt="Image of web page showing valid validation results."
%}

Validation by URI is the best way to ensure the HTML file that you are turning in is valid. If you do this right before you create the pull-request for the grading branch, you can be 99% sure that you are validating the same thing that I will be validating when I grade your assignment.  (I say 99% on the off-chance that you update the file again after you validate and do not re-validate again. If you update the file, it's important to validate again.)

### Validate by File Upload
Before you push your HTML file up to GitHub, it's helpful to validate your work using the HTML file on your computer.  The "Validate by File Upload" tab allows you to do this.  If you click on this tab, you are able to select a file from your computer to upload to the Validator.

{% include img-medium.html url="/assets/images/intro-valid-html/validate-by-file.png"
    alt="Image of Validate by File Upload tab showing the where to click to select a file to validate."
%}

### Validate by Direct Input
The last tab, "Validate by Direct Input", provides an alternative to uploading your file for validation. If you click this tab, it provides a text box where you may paste in the HTML you want to validate. I do not recommend this approach however as it is easy to miss part of the HTML, forget to save the file, or otherwise have differences between the HTML you validate and the file you upload to GitHub.

### More Info
Additional information on validation can be found on the [W3C website](https://www.w3.org/wiki/Validating_your_HTML).


## Validation Tips
Students often find validation errors intimidating at first. My best advice is "Don't panic." If you have errors, take a deep breath, relax and then follow the tips below to work through them.

- First, note that warnings are not errors and are not required to be fixed.

- Work through the errors one-by-one starting at the top. Make a fix, then validate again. Often you will fix one validation error and find that it actually resolves many or most of the others too.

- Read the error message. It will tell you the line number where it noticed the error. That is not always the exact location of the error, just due to the nature of the way the validator works, but it is usually correct and if not it is often very close.

- Recognize that most often, validation errors are caused by simple typos (that can be hard to spot):
  - You must type your tag names and attribute names correctly.
  - You can't forget an opening or closing < or > on your tag.
  - Closing tags need the </ so they are not considered opening tags.
  - Attributes must have their values in quotes.

- There can only be one `body`, and it is assumed if not seen before the first content markup tag. The opening `body` tag should immediately follow the closing `head` tag. If you put it in the wrong place, you may get the error "Stray start tag 'body'."

- There are some things that can only occur once on a page:
  - the `main` tag
  - id attribute values must be unique on a given page, so they can't be found twice

- Some tags must be children of particular elements. For example the `li` element must be in either a `ul` or `ol` element.

- Some tags cannot be children of other tags. For example, you can't have a `ul` element as a child of a `p` element.  When the `ul` is seen, it is assumed to end the `p` element, so a closing `</p>` tag after the `ul` will give a validation error.

There are many different errors that you might bump into, and this list only helps with things I've found in the past to be the most common errors. If you need help with other errors, just let me know. I'm glad to help.

### If you need help...
If you get a validation error you are unable to resolve:
- push your code to GitHub, so that I can view your HTML
- then send me an email that includes a link to the HTML page on GitHub and the text of the validation error

I'll follow up with you as soon as I can with advice on how to resolve the error.
