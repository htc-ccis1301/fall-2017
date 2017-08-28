---
title: "Fan Page Part 1"
summary: "Build a web page about something you really like using the HTML elements we have learned."
---

# {{ page.title }}
{{page.summary}}


This will be the first of a multi-part assignment in which you will create a fan page for something you enjoy: a movie, game, band, or even your favorite food or restaurant.  You choose the topic, but make sure that your topic choice is *professional* (not something embarrassing to show at a job interview).

{% include alert.html type="warning"
  content="As you build this site, be careful in the use of images, text, and other content from other sources. I expect that if you use the material of others that you both have permission to use the material and that you credit the content owner either near the content itself or in the page footer."
%}


## Prerequisites
Completion of this exercise requires an understanding of the material from earlier modules and from:

- [HTML Template Explained]({{ "/readings/intro-template-html.html " | prepend: site.baseurl }})
- [HTML Basics]({{ "/readings/intro-basic-html.html " | prepend: site.baseurl }})
- [HTML Validation]({{ "/readings/intro-valid-html.html " | prepend: site.baseurl }})

## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment - Fan-Page]( https://classroom.github.com/a/UuuqkKTQ )

Note that once you accept this assignment for part 1, you will continue working with the same repository on GitHub for later parts of the assignment and will not need to accept the assignment again.

## Requirements
Using Brackets and the template HTML introduced in the reading to make a basic HTML page. You should call this page index.html, as that is the default home page for most web servers.

Then update the page to include the following:

- A title that reflects the favorite thing you are building the site for
- A link to a different website or other information about this thing.
- A summary of what this thing is and what you like about it.
- A list of something (ordered or unordered).
- A header with the site name
- At least two subheadings.
- A footer with copyright information.  You own the copyright to your own page, so use your name and the current year.
- An email contact link for you in the footer.  To avoid putting your real email on the page you can use yourFirstName@yourLastName.com or something like that, so long as it is a proper email link, I don't care if it actually works.

Do not neglect the <head> section and HTML structural elements just because they are not visible on the web page. Your head section must include a title and the charset.  Your page should include at a minimum the header, main and footer structural elements.

Once you have verified your work, version and push it up to GitHub.  

### Publish to the web
Once your changes are on GitHub, create a pull-request to move the changes from the __dev__ branch to the __gh-pages__ branch. After creating the pull-request and reviewing the changes, merge the changes to publish your work to the web.  Make sure to repeat your testing and validation using the published web site.


## Submit the assignment
When everything looks good, create the pull request for the grading branch to have your work graded. Remember, __DO NOT MERGE__ this pull request. For the work to be graded, the pull-request must be left open.  

Submit the following screenshots (in one MS Word document) to the Assignment box on D2L:

- The Open pull-request for the __grading__ branch
- The actual web page as published on GitHub Pages (URL in Settings)
- Validation of HTML file using the W3C Validator

You __must__ capture URL at the top of the browser display and the page contents for the screenshots.

You can continue working on the Fan Page assignment locally and push updates to the __dev__ branch, but please do not merge any changes to __gh-pages__ until the previous work for the assignment has been graded. I will aim to have feedback to you within a few days of your submission, so you won't have to wait long.
