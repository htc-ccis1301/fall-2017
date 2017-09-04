---
title: "Fan Page - Part 2"
summary: "Let's add some CSS to give our Fan Page a bit of style!"
---

# {{ page.title }}
{{page.summary}}

## Prerequisites
Completion of this exercise requires completion of the previous assignments:  

- [Fan Page - Part 1]({{ "/experiences/fan-page-pt1.html " | prepend: site.baseurl }})


It also requires an understanding of the material presented in earlier modules and the readings:  

- [Styling with CSS]({{ "/readings/css-intro.html " | prepend: site.baseurl }})
- [Colors in CSS]({{ "/readings/css-colors.html " | prepend: site.baseurl }})
- [Styling Text]({{ "/readings/css-styling-text.html " | prepend: site.baseurl }})


## Continue the assignment
Since this is a multi-part assignment, you will continue working with the website and repository from Part 1 by updating the existing index.html file and adding a new CSS file.

You will continue to improve and enhance this web page throughout the first part of the course. When you are finished with the last part of the assignment, you should have a page that you might use on your online resume.

You should see your repository from the previous assignment here:
[ {{ site.data.github-info.org-name }} ]( {{ site.data.github-info.org-url }} )

If you did not complete the first part of the assignment, you will need to go back and do that before beginning part 2. There is a link to the earlier assignments in the Prerequisites section above.

## Requirements
For this assignment, you will continue work with your fan page project and GitHub repository. You will *update* the HTML page that you created for part 1 adding images and a new CSS file to the site.

__All__ styles must be placed in the external stylesheet.  You should not include any CSS in your HTML page.  This is a general best practice as it supports easier maintenance of your web site.  Does it make sense to you why that might be true?

### Add Images
Add a new directory (folder) to your project to hold the image files for your site.

Update your web page to include a small (thumbnail) image with a caption that is also a link to a larger version of the same image.  Make sure to include two image files, one for the thumbnail and one for the larger image.  Don't just resize the larger image for the thumbnail.  That is a bad practice as it slows the page load and wastes bandwidth.

{% include alert.html type="warning"
  content="As you build this site, be careful in the use of images, text, and other content from other sources. I expect that if you use the material of others that you both have permission to use the material and that you credit the content owner either near the content itself or in the page footer."
%}

### Style Updates
Add a new external stylesheet called style.css to your website project folder, and update your index.html page to use your new stylesheet.

Update the HTML & CSS to have (at a minimum) the following items:

- a new document background color
- a new default document text color
- a different font (use a full font-stack) for the default document text
- an element with an id that is used by CSS to change the background or text color
- a `<span>` with a style class that is used by CSS to change the text color
- a different font (use a full font-stack) for one level of headings (h1, h2, etc.)
- capitalize (all caps) for one level of headings (h1, h2, etc.)
- change the font color for one level of headings (h1, h2, etc.)
- italicize and decrease the font size for the footer
- use a different list marker
- bold and increase the font size for your link to the other web page
- remove the underline from the link to the other web page
- add a div with a background image to page
- add a favorite icon to your page

{% include alert.html type="warning" content="Use the [CSS Font Stack](http://www.cssfontstack.com/) site to help you select a full font-stack for the font family list. (We discussed what makes a good font-family stack in the reading notes.)" %}


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
