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

## More Coming Soon...
This page is still being written.

## Review Questions

- What is the purpose of the `<!DOCTYPE html>` tag?
- What is the difference between an opening tag and a closing tag?
- What are the two main sections of an HTML document?  What is each used for?
- What is an attribute?  Give an example of a tag that requires and attribute.
- What is the purpose of the `<title>` element? Can it be seen when viewing a page in the browser?
- What is a charset?  How do you tell the browser which charset it should use?
- What name should you use for the main or "home" page of a website?
