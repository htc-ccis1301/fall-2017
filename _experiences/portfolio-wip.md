---
title: "Portfolio: Work In-Progress Review"
summary: "Build an initial outline of your site before adding custom content and styling."
---

# {{ page.title }}
{{ page.morea_summary }}

{% include alert.html
    type="danger"
    content="Remember that your wireframes are our  __*contract*__  for this assignment. If your site does not match your wireframes, points may be deducted for any differences."
%}

## GitHub Project
Click the link below, then click the green button to accept the assignment.

[Final Project: Web Portfolio]( https://classroom.github.com/a/OOXdnG97 )


## Outline
To get some initial feedback on your developing portfolio site, you may optionally submit an outline of the site focusing mainly on HTML and Bootstrap. This is intended to get you some early help using Bootstrap if it is needed. This also allow you a chance to have me do a preliminary review of your site layout and design. The more you have done, the more I can review and give you feedback on.

Consider what we did with Ms. B's website.  It looked pretty ho-hum and standard, right up until that last few minutes as we started tweaking the CSS.  Get the HTML foundation in place, use default Bootstrap components, and later work on adding the content details and making the style unique.

Try not to get too caught up in the content itself as you build the site outline.  Use [Lorem ipsum](http://www.lipsum.com/) text if needed to avoid getting caught up writing. Use placeholder images, or just a `<div>` with a size, background-color and "Image TBD" text for now.  The details can come later.  

## HTML5 Elements
Make sure that you are using HTML5 structural tags to outline your site.  You should have at a minimum, the `nav`, `main`,  `article` and/or `section` tags (for each of the required content sections), and a `footer`.  The header is not necessary, as it is generally incorporated into the Bootstrap `nav`.  You may include a separate `header` if you wish, so long as it doesn't interfere with the Bootstrap navbar and scrollspy behavior.

Once you have verified your work, version and push it up to GitHub.  

### Publish to the web
Once your changes are on GitHub, create a pull-request to move the changes from the __master__ branch to the __gh-pages__ branch. After creating the pull-request and reviewing the changes, merge the changes to publish your work to the web.  Make sure to repeat your testing and validation using the published web site.


## Submit the assignment
When everything looks good, create the pull request for the grading branch to have your work graded. Remember, __DO NOT MERGE__ this pull request. For the work to be graded, the pull-request must be left open.  

Submit the following screenshots to the Assignment box on D2L:

- Open-pull request
- Actual web page as published on GitHub (URL in Settings)
- Validation of HTML & CSS files by URL. (You are not responsible for the Bootstrap CSS only your own.)

{% include alert.html
    type="danger"
    content="To received a full in-progress site review, a pull-request must be made before the due date. Any pull-requests submitted after the due date or without a screenshot in the assignment box on D2L are not guaranteed to be reviewed before the final project is due. I will answer specific questions and help troubleshoot the project through the final due date but will not do full site reviews for feedback after this date."
%}
