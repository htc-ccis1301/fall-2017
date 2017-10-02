---
title: "Fan Page - Part 3"
summary: "Let's add images to give our Fan Page and improve the overall page layout and style."
---

# {{ page.title }}
{{page.summary}}

## Prerequisites
Completion of this exercise requires completion of the previous assignments:  

- [Fan Page - Part 1]({{ "/experiences/fan-page-pt1.html " | prepend: site.baseurl }})
- [Fan Page - Part 2]({{ "/experiences/fan-page-pt2.html " | prepend: site.baseurl }})

It also requires an understanding of the material presented in earlier modules and the readings:  

- [Web Graphics]({{ "/readings/web-graphics.html " | prepend: site.baseurl }})
- [CSS Box Model]({{ "/readings/css-box-model.html " | prepend: site.baseurl }})
- [Styling for Images & Layout]({{ "/readings/css-more-styles-more.html " | prepend: site.baseurl }})
- [Page Layout & Design]({{ "/readings/design-layout.html " | prepend: site.baseurl }})

## Continue the assignment
Since this is a multi-part assignment, you will continue working with the website and repository from Part 1 by updating the existing index.html file and adding a new CSS file.

You will continue to improve and enhance this web page throughout the first part of the course. When you are finished with the last part of the assignment, you should have a page that you might use on your online resume.

You should see your repository from the previous assignment here:
[ {{ site.data.github-info.org-name }} ]( {{ site.data.github-info.org-url }} )

If you did not complete the first parts of the assignment, you will need to go back and do that before beginning this assignment. There is a link to the earlier assignments in the Prerequisites section above.

## Requirements
For this assignment, you will continue work with your fan page project and GitHub repository, updating the HTML & CSS pages that were previously created.

Note that many of these requirements pull from topics covered in the earlier modules as well.

### More Content
Add *at least* two more subheadings (for a total of four) to your page. Each subheading should have text and/or image content following it.

Use HTML5 article and/or section tags to group and organize related content.

### Images
{% include alert.html type="warning"
  content="As you build this site, be careful in the use of images, text, and other content from other sources. I expect that if you use the material of others that you both have permission to use the material and that you credit the content owner either near the content itself or in the page footer."
%}

1. Add a new directory (folder) to your project to hold all the image files for your site.

2. Update your web page to include a small (thumbnail) image.

3. Set up the thumbnail to link to a larger version of the same image.  (Make sure to include two image files, one for the thumbnail sized image and one for the larger image. Don't just resize the large image to show as a thumbnail.)

4. Add a larger image with a caption that is styled to look like a polaroid image.

5. Add a small background image to an element so that it is positioned to the side of the content and does not fill the entire element space. (For example it sits to the right side of a heading or list.)

6. Use a *very* small image as a list marker.

7. Add a favicon to your page.

### Layout

1. Set up the `header` to span the full page width. 

2. Set a width of 80% on the `main` content and center it within the page using auto margins.

3. Use padding on the `main` element to set the content away from the edges (element border).

4. Use margins to separate headings from the previous content above.

5. Style some element to have a solid, contrasting colored border on one or two sides.

You should try to set up the spacing from padding & margins to roughly represent the 60-30-10 rule.

### Additional Styling
1. Set the `html` element to have a gradient background.

2. Set either the `main` or `article` and/or `section` content to have a solid background color with a contrasting, readable text color.

3. Style some element to have a box shadow.

4. Add a semi-transparent background color and rounded corners to one or more headings.

5. Add a text shadow to one level of page headings.


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
