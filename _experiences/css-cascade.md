---
title: "CSS Cascade"
summary: "An exercise to explore in more detail the way CSS is applied and how the CSS Cascade rules work."
---

# {{ page.title }}
{{ page.summary }}


## Prerequisites
The following topics were covered earlier:

- [Styling with CSS]({{ "/readings/css-intro.html " | prepend: site.baseurl }})
- [Colors in CSS]({{ "/readings/css-colors.html " | prepend: site.baseurl }})
- [Browser Developer Tools]({{ "/readings/dev-tools-intro.html " | prepend: site.baseurl }})


## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment - CSS Cascade]( https://classroom.github.com/a/9VIxm6Nh )


## Requirements
Clone the repository to your local computer, and then open the project folder in Brackets.  Notice that you have an HTML file and a CSS file provided for you.  If you view the web page, you'll see that it should look like this:

{% include img-medium.html url="/assets/images/css-cascade/initial-page.png"
    alt="Screenshot of initial web page."
%}

Update the information in the `footer` to use your name, and update the "Replace this text" in the ordered list to include 3 things you like about what you are learning in the class. Then follow through the steps in each section below to explore how different types of CSS are used and how they interact with each other.


## Inherited CSS
When CSS is applied to a selector, it affects the entire element selected, including its child element. This makes it easy to setup default style rules for a web page by creating a rule for the `body` element. When we apply style rules to the body, it also affects all of the elements in the body, or all of the elements shown on the page. This is a great way to setup a website's basic color and text styles.

In the CSS file for the assignment, there is a CSS rule specified for the `body` element. It sets the background color of the page to a light purple (#E6E6FA), and the foreground (or text color) to be dark purple (#191970).  

What will happen if we create an additional rule that sets a different background-color for paragraphs, child elements of the body?  Which color will the browser use for the paragraphs when it displays the page? Let's experiment to see.

1. Add a new style rule to the external CSS file to give paragraph elements a medium purple background color (#AEAED4).

2. Look at one of the paragraph elements using the developer tools.  Notice that the inherited style for the background color from the body is crossed out.
{% include img-medium.html url="/assets/images/css-cascade/inherited-applied-p-style.png"
    alt="Screenshot of CSS applied to p tags to change background-color."
%}

Notice that while this changed the background-color, it did not affect the text color.  The paragraphs no longer use the inherited background-color, but they still inherit the color property that controls the text color.

This is part of the cascading nature of CSS rules. Parent rules cascade down to their children, unless another rule takes precedence over the inherited style.  Understanding how and when styles rules are overridden is a very important part of learning CSS.

{% include alert.html type="tip"
    content="When you are applying CSS to an element on a web page and you do not see the desired result, use the developer tools to see if your style is being overridden by another rule. Notice in the example above that the developer tools shows the exact file and line number of the location of the applied CSS. This is extremely helpful when solving problems with page display."
%}


## Overrides
What happens when two rules affect the same element?  How does the browser know which rule to use? Again, let's experiment with this to see what will happen.

1.  Add an id attribute to one of the paragraphs in the main content.  You can name the id whatever you would like and apply it to any one of the paragraphs in the main element.  

2.  Add a CSS rule to the external CSS file to change the background-color of that ID to be white.

3.  We now have two rules that should apply to that paragraph.  Use the developer tools to see the CSS applied to that paragraph.  
{% include img-medium.html url="/assets/images/css-cascade/id-override-p-style.png"
    alt="Screenshot of CSS applied to p tag by id."
%}

Notice that the browser did apply the `p` element rule, but then for the paragraph with the id, the rule is crossed out.  This means that the rule is overridden by another rule that applies to the same element.  

### Specificity
Because the style rule for ID is more specific than the style rule for all HTML p elements, the browser uses the ID rule.  Rules that are more specific win.

We do not need to use id's to be more specific.  We can also use style classes or descendant selectors. A style class is more specific than an HTML tag name, an ID is more specific than a style class.  

Using HTML tags in a descendant selector is also more specific than using a single HTML tag, but when style classes or id's start to be involved, things can become more complex.  We'll leave it at this for now, but if you want to know more, checkout the [official rules](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity).

### Last one in wins
If there are two rules that are equally specific, the last one in wins.  

1.  Add a second CSS rule __to the end__ of your external style sheet that will change the background-color of the paragraphs to be red.  

2.  Again look at the applied CSS using the developer tools.
{% include img-medium.html url="/assets/images/css-cascade/last-in-wins.png"
    alt="Screenshot of two CSS rules applied to p tag."
%}

Notice the line numbers.  The CSS file is read top to bottom, and the color will be set by the CSS rule that is read last.  Last one in wins!

When you're done exploring the page with the Developer Tools, __take out this red paragraph rule__.  It's not so pretty with the purples!

{% include alert.html type="tip"
    content="Style bugs are often introduced by having multiple rules for the same selector. Before adding a new rule to your CSS file, look through the rules you already have to make sure that there is not an existing rule for that selector. If there is, just add additional properties to the same rule instead of adding a new one."
%}


## Embedded & Inline CSS
It is important that you understand how external, embedded, and inline CSS work together. Your understanding of this will be checked through quizzes and exams.  *However* for all your assignments (except for this one) you should use *only* external CSS.  

The browser has default styles built in. These are usually overridden by external CSS styles. The external CSS styles may also be overridden by embedded CSS styles, which then might be overridden by inline CSS styles.

{% include img-medium.html url="/assets/images/css-cascade/basic-css-cascade.png"
    alt="Image of CSS Cascade: browser styles are overridden by external styles which are overridden by embedded styles which are overridden by inline styles."
%}

### Embedded CSS
Add an embedded style to the index.html file to set the paragraph background-color to blue (#A6C6DF). You should now see that your paragraphs are blue. Use the developer tools to look at the applied CSS.

{% include img-medium.html url="/assets/images/css-cascade/embedded-override-external.png"
    alt="Screenshot of embedded style overriding external."
%}

Notice that the embedded style (from the HTML file) overrides the rule set-up in the external stylesheet.

### Inline CSS
Next, let's look at how inline styles are applied.  Choose one of the paragraphs that does not have the ID attribute applied, and add an inline style to it to set the background-color to light blue (#D3E5F3). You should now see that one paragraph is now a lighter blue. Use the developer tools to look at the applied CSS.

{% include img-medium.html url="/assets/images/css-cascade/inline-override-both.png"
    alt="Screenshot of inline style overriding both embedded and external."
%}


## Descendant Selectors
Descendant selectors in CSS are very important.  They get used __a lot__ because they help you to be more specific without the need for adding extra stuff into your HTML.  Let's say that we want to have all of the paragraphs in the main content get their background-color from their parent element.  

Let's add this new rule to our external stylesheet. First we need to know how to write the selector to get only paragraphs that are inside the main element.  

{% highlight bash %}
main p {

}
{% endhighlight %}

Next question is how do we know what the background-color of their parent element is? It could be different for each paragraph, right?  They may not all be direct children of the `main` element.  (Notice the one that is a child of a `div` which is then a child of `main`.)  To have an element use the value of its parent, we can use the word `inherit` as the value of the property.

{% highlight bash %}
main p {
  background-color: inherit;
}
{% endhighlight %}

Now what color do you expect the background-color for paragraphs to be?  Will they all have the same background-color, or do you think some will still be different?  Think about this before you try it out.  If things are different than what you expected, see if you can figure out why.  Use the developer tools to help you.

{% include alert.html type="tip"
    content="You don't need to use inherit very often because it is the default behavior.  You would only need to use it to *undo* other applied CSS, much like we are doing here."
%}


## Review Questions

- How do you add embedded CSS to a web page? How do you add an inline style?
- What is the difference between an embedded style and an inline style?
- What effect does the CSS applied to a parent element have on its children?
- Why is it considered a bad practice to use embedded and inline styles?


## Publish & Submit
Once your changes are on GitHub, create a pull-request to move the changes from the __dev__ branch to the __gh-pages__ branch. After creating the pull-request and reviewing the changes, merge the changes to publish your work to the web.  Make sure to repeat your testing and validation using the published web site.

When you are ready to submit you work, create the pull-request for grading. Remember, __DO NOT MERGE__ this pull request. For the work to be graded, the pull-request must be left open.  Make sure to take a screenshot of the open pull-request to put in the assignment box on D2L.

Submit the following screenshots (in one MS Word document) to the Assignment box on D2L:

- Open-pull request
- Actual web page as published on GitHub (URL in Settings)
- Validation of HTML files by URL
- Validation of CSS file
