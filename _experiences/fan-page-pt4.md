---
title: "Fan Page - Part 4"
summary: "Let's setup different layouts for our page based on the size of our browser dispaly."
---

# {{ page.title }}
{{page.summary}}

## Prerequisites
Completion of this exercise requires completion of the previous assignments:  

- [Fan Page - Part 1]({{ "/experiences/fan-page-pt1.html " | prepend: site.baseurl }})
- [Fan Page - Part 2]({{ "/experiences/fan-page-pt2.html " | prepend: site.baseurl }})
- [Fan Page - Part 3]({{ "/experiences/fan-page-pt3.html " | prepend: site.baseurl }})

It also requires an understanding of the material presented in earlier modules and the readings:  

- [CSS for Page Layout]({{ "/readings/css-layout.html " | prepend: site.baseurl }})
- [CSS Responsive Layout]({{ "/readings/css-responsive.html " | prepend: site.baseurl }})

## Continue the assignment
Since this is a multi-part assignment, you will continue working with the website and repository from Part 1 by updating the existing index.html and CSS files.

You will continue to improve and enhance this web page throughout the first part of the course. When you are finished with the last part of the assignment, you should have a page that you might use on your online resume.

You should see your repository from the previous assignment here:
[ {{ site.data.github-info.org-name }} ]( {{ site.data.github-info.org-url }} )

If you did not complete the earlier parts of the assignment, you will need to go back and do that before beginning this assignment. There is a link to the earlier assignments in the Prerequisites section above.

## Requirements
For this assignment, you will continue work with your fan page project and GitHub repository, updating the HTML & CSS pages that were previously created.

Note that many of these requirements pull from topics covered in the earlier modules as well as the current module.

### Image Gallery
Add a small image gallery of 5-10 images. Use an inline-block layout to have the images flow and wrap nicely based on the width of the browser display.

### Desktop Layout

#### Header

1. Set up the `header` to span the full page width.
2. Center the text in the header.
3. Fix the `header` at the top of the page so it stays in the same position when the page content scrolls.   
4. Ensure that no content is hidden under the header on page load or when using the in-page navigation.

To test the header, you may need to reduce the height of your browser window to test the links & content positioning with scrolling.

#### Navigation

1. Reorganize your `nav` to contain an HTML list of all of the links.
2. Apply CSS to the list items so that they are displayed in a single line across the page with no list marker.
3. Center the links across the top of the page.

With the navigation list, you will need to adjust the styling of both the list (`ul`) and its list items (`li`). Examine the box-model styles for the `ul` and `li` elements in the browser developer tools, adjusting the margin and padding on each appropriately for a nice layout.

#### Main content

The following should have been done in Part 3:
1. Center the `main` content on the page at 80% width.
2. The main content should have a solid background color with a contrasting text color.
3. A gradient background (from the html element) should show down the sides of the main content.

New:
1. Float the larger polaroid image to the right side of some content, allowing text to flow around it.


### Tablet Layout

Main content:
1. Set the width of the main content to 100% of the display. The gradient background should no longer be visible down the sides.


### Mobile Layout

Header:
1. Set `header` to scroll normally with the page content allowing more content view space.

Navigation:
1. Stack the navigation links (one on top of the other).
2. Have each *link* (not just the list item, but the clickable link) span the full width of the page.

Main content:
1. Hide the larger "polaroid" image.
2. Reduce the page default font size to 90%.
3. The tablet behavior to have the width at 100% should also apply to mobile.


Once you have verified your work, version and push it up to GitHub.  


### Publish to the web
Once your changes are on GitHub, create a pull-request to move the changes from the __dev__ branch to the __gh-pages__ branch. After creating the pull-request and reviewing the changes, merge the changes to publish your work to the web.  Make sure to repeat your testing and validation using the published web site.


## Submit the assignment
When everything looks good, create the pull request for the grading branch to have your work graded. Remember, __DO NOT MERGE__ this pull request. For the work to be graded, the pull-request must be left open.  

Submit the following screenshots (in one MS Word document) to the Assignment box on D2L:

- The Open pull-request for the __grading__ branch
- The actual web page as published on GitHub Pages (URL in Settings)
- Validation of HTML file using the W3C Validator
- Validation of CSS file

You __must__ capture URL at the top of the browser display and the page contents for the screenshots.

You can continue working on the Fan Page assignment locally and push updates to the __dev__ branch, but please do not merge any changes to __gh-pages__ until the previous work for the assignment has been graded. I will aim to have feedback to you within a few days of your submission, so you won't have to wait long.
