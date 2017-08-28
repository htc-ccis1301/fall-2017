---
title: "HTML Template Explained"
summary: "A review of the basic HTML5 template introduced earlier with an explanation of each of the parts that make up the template page."
---

# {{ page.title }}
{{page.morea_summary}}

## HTML Template
Remember this basic HTML template that we used in the first module?

{% gist mbMosman/5785c6e9534e956b79d7 basicHTML5.html %}

Now let's learn a bit more about it. We'll go through the structure of this template piece by piece, or in better HTML terminology, element by element.

{% include alert.html type="warning"
    content="Be very careful with your typing. Make sure that you get every single key correct. A missing quote or angle bracket <> can be hard to find and cause problems with the display or page validation."  
%}  

### DOCTYPE
The `DOCTYPE`, or Document Type Declaration, is used to identify what type of markup a document is written in. The doctype for HTML5 is quite simple:
{% highlight html %}
<!DOCTYPE html>
{% endhighlight %}

This basically says "Hey browser, this document is written in HTML5".

However older HTML DOCTYPEs were a little more complex.  You don't need to memorize or even use these, but you should be aware of what they look like in case you ever come across them. Note in each of the following examples where you see the version name & number.  __I expect that if given an older DOCTYPE you can tell me what type of HTML the document is written in.__

HTML 4.01 looks like this:
{% highlight html %}
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
{% endhighlight %}

And XHTML 1.0 looks like this:
{% highlight html %}
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict //EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
{% endhighlight %}

The reason that the HTML5 `DOCTYPE` is so simple is that previous standards were not necessarily backward and forward compatible, so it was really important that the browser knew exactly what syntax the author expected the page to be rendered with. HTML5 makes standard a new expectation that future HTML standards are backward compatible, so things written for HTML5 should behave acceptably in that future HTML6 or HTML7 browser. This is a breath of fresh air to the HTML standards world.

## The HTML Element
The next element in the template is the `html` element. Notice that it has an opening tag `<html lang="en">` on line 2 and a closing tag `</html>` on line 13. Closing tags in HTML begin with the / before the element (or tag) name. Most, but not all HTML elements will have both an opening and closing tag.

Also notice that the opening tag consists of the name of the element `html` plus `lang="en"` which is an __attribute__.  An attribute is a name-value pair. The attribute name is "lang", and the value of the attribute is "en". Attribute values are always contained in quotes. As you might guess the purpose of this attribute is to tell the browser which language the document content is written in.

The `html` element is required to be present in all HTML documents, and all of the other HTML elements that make up the page must be contained between the opening and closing tag of the `html` element for the document to be valid.

The `html` element must have both a `head` and a `body` element as its contents. That means that the `head` and `body` elements (which will be discussed below) must be found between the opening `<html>` tag and the closing `</html>` tag. The `head` and `body` are called __child elements__ of the `html` element. This __parent-child__ relationship will be discussed further in the Reading: [HTML Document Structure]({{ "/readings/intro-dom.html " | prepend: site.baseurl }}).

The `head` and the `body` divide the HTML document into two main sections:

- the `head` contains information for the browser about the page and how it should be displayed
- the `body` contains the content to be displayed in the browser window


## The Head Element
The `head` element, lines 3-7, comes next. The `head` is one of the two required elements that must be found in (or between the opening and closing tag of) the `html` element. The `head` element is used to provide additional information to the web browser that is needed in order for it to display the HTML page properly.

### Title Element
The `title` element, shown on line 4, is the one piece of information from the `head` that is visible to a visitor to the page on the Web.  It is used as the name of the browser window or tab in which the page content (from the `body`) is displayed.

The `title` is a required element in the `head`; you will get a validation error if it is not present.  

### Link Element
The `link` element, example on line 5, is an optional element in the `head`. If present, it is used to include additional files in a web page. It is generally used to add CSS files or stylesheets, but can also be used to include icons and other items. The type of information is determined by the value of the `rel` attribute and the file itself is identified by the URL provided as the value of the `href` attribute.

The example `link` attribute on line 5 is not valid because there is now value given for the `href` attribute.  When no stylesheet is added, this element should be deleted from the template. However, beginning with Module 3, our HTML pages will always include a stylesheet so it will be handy to keep this in the template for future use.

### Meta Element
The `meta` element is an optional element used in the `head` to provide various types of page metadata, or information about the page. The example `meta` element on line 6, is used to tell the browser which `charset`, character set or character encoding, to use when displaying the content of the page. The example shown uses the `utf-8` charset which is the default charset for HTML5. [UTF-8](https://en.wikipedia.org/wiki/UTF-8) supports basic unicode and is able to display nearly all of the characters in use around the world today.

While this element is not required in order for the page to be valid, it is a best practice to include the `charset` information on all pages for compatibility with older browser (which may assume a different default).  It will be expected that the `charset` is present for all work in this class.

There are many other possible uses of the `meta` tag, and we will learn a few more of them later in the course.  

## The Body Element
Next, on lines 8 - 12, we have the `body` element. It the second of the two required child elements of the `html` element. The `body` element is used to contain all of the page content or the things that appear on the page when viewed in a web browser.

Here the body tag only contains a `p` or paragraph element with the text "Replace me with your content." However there are many different HTML elements that are used to markup the content of a web page so it can be displayed nicely in a browser. We will begin to learn more of these in the Reading: [HTML Basics]({{ "/readings/intro-basic-html.html " | prepend: site.baseurl }}), and continue learning more throughout the course.

## Review Questions

- What is the purpose of the `<!DOCTYPE html>` tag?
- What is the difference between an opening tag and a closing tag?
- What are the two required child elements of the `html` element?  What is each used for?
- What is an attribute?  Give an example of a tag that requires and attribute.
- What is the purpose of the `<title>` element? Can it be seen when viewing a page in the browser?
- What is a charset?  How do you tell the browser which charset it should use?
