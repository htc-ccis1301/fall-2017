---
title: "HTML Basics"
summary: "An introduction to basic HTML elements used to structure content on a web page."
---

# {{ page.title }}
{{ page.summary }}

## Headings & Paragraphs
The two most commonly used elements on an HTML page are headings and paragraphs.  These elements help you structure the page content by providing headings that summarize the content that follows in one or more paragraphs. The headings should outline the page content, while the paragraphs provide the details.

There are six heading tags to represent different levels of content they range from `h1` to `h6`. To use a heading on your page, put the text that you want to see between the opening and closing tags of the appropriate level.

Here are some examples:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="brxjPX" height="340"
%}

It's important that you choose which heading element to use based on the outline of the page structure, not it's default display size.

There is generally only one `h1` element on a page, and it is used for either:

- The site name
- The page title

If the `h1` is used for the site name, then the `h2` should be used for the page title. The remaining page content is then outlined using one or more `h3` - `h6` subheadings. When the `h1` is used for the page title, the subheadings outlining the page content can begin with `h2`. It's important to structure headings and content correctly to assist both search engines and screen-reader users.

The detailed information following each heading is placed into a `p` (paragraph) element. Just like when writing an English paper, related sentences should be grouped into paragraphs. This helps to make reading long page content feel more natural, just like reading a book or paper.

## Lists
Where would we be without lists of things?  Lists are everywhere, including in HTML. We have two main types of list elements that we can use: ordered or numbered lists & un-ordered or bullet lists. Ordered lists use the `ol` element, while un-ordered lists use the `li` element. Both types of list use the `li` element for each of the list items.

Here is an example of an ordered list:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="brxjOy" height="175"
%}

Here is an example of an ordered list:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="wqExOb" height="175"
%}

You can also put lists inside of lists by including a `ul` or `ol` as a child of a `li` element.

{% include alert.html type="warning"
    content="The `ul` and `ol` elements can only contain `li` children.  If you place the sublist `ul` or `ol` inside the `ul` or `ol` instead of inside one of their child `li` elements, you will get a validation error."
%}

Here is an example of nesting lists:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="wqYvqY" height="430"
%}



## Links
The *HyperText* in HTML - HyperText Markup Language - comes from the idea that you have *HyperLinks* or embedded reference links to other documents and content. This was a great improvement over the standard references you might have had in a paper document, as you could go directly to the linked content for more information. These links really made the Internet what it is today, and it's hard to imagine not having them.

Links are created by using `a` (anchor) elements. The text for the link, goes in between the opening and closing tags. The `a` element is required to have an `href` __attribute__ that contains the URL of the resource that you want to link to. These URLs can take two forms:

- absolute URLs - the full web address of a resource, usually on a different website
- relative URLs - a path to a resource on the current site, relative to the current file


Here are some examples:
{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="RZYYRv" height="250"
%}

### In Page Links
There are times where it is helpful to link to content in the same page, for example to include a table of contents that links to various headings in a long page. To do this, you need both a *target* and an *anchor*.  The target is an HTML tag in the page that has an `id` attribute added to it. Any HTML element can have an `id` attribute added to it. The anchor is of course the `a` element.

{% include codepen.html username="mbMosman2" author="Mary Mosman"
      embedcode="NvLLpG" height="250"
%}

{% include alert.html type="danger"
    content="The value of the `id` attribute is required to be unique on a page. That means the same `id` can be used on different pages, but it can only appear once within the same page."
%}


### Other Links
There are also a few types of specialized links. For these links, the `href` attribute is modified to indicate the type of reference.  The most common of these specialized links is a link to an email address. Note the `mailto:` in the email link below:

{% highlight html %}
<a href="mailto:mary.mosman@hennepintech.edu">Email Mary</a>
{% endhighlight %}

Another specialized link is for a telephone number. This type of link can be handy when websites are viewed on a mobile phone. Note the `tel:` in the phone link below:

{% highlight html %}
<a href="tel:123-456-7788">123-456-7788</a>
{% endhighlight %}

## HTML5 Page Structure
The latest version of HTML includes new elements that help to provide additional information about the structure of the page. These new elements are more informational than visible, and are intended to contain other HTML elements, such as the ones we learned above. These elements may be helpful to screen-readers in helping users to navigate the HTML page in a meaningful way.

### Header, Nav & Footer
Many websites have a common header across the top of all pages of the site and a common footer along the bottom. The HTML5 `header` and `footer` elements can be used to help structure this content on a page.  The header often contains the name of the site and a logo image. The footer often contains copyright and contact information. The `footer` element might also contain additional links that are less important to the main purpose of the page.

HTML5 also adds a `nav` element to structure and group the navigation links for a page. This grouping of navigation links not only provides page structure, but may also better support users of screen readers. The main site navigation may be added into the `header` or may be kept separate. The choice is often determined by the site design and the way these elements are intended to be styled using CSS. We will talk more about this in later modules.

### Main Content
The main content of the web page should be placed inside of the new `main` element. This content should be the focus of the page, the *main* attraction so to speak. The `main` element will contain other elements such as headings and paragraphs, describing the main topic.

### Articles & Sections
HTML5 also added the `article` and `section` elements. These elements can be used to group related content on larger pages. For example a blog may show a series of posts from different times, and each might be contained within an `article` element. A page with a lot of content might also benefit from grouping related content into `section` for different subtopics. The use of these is less well defined and the two elements can be used separately or together.

### Aside
The last of the new HTML5 structure elements is the `aside`. The aside should contain content that is related but not essential. It's purpose is contextual depending on if it is at the page level or contained within an `article` or `section`. At the page level it might contain ads, a search feature, or link to other sites with related information. Within an `article` or `section` it might contain references, a glossary, or other supplemental information.

### Page Division
These new structural tags replace the use of the more generic `div` element to structure a page for styling and presentation. For example, you would often that a page would have a `<div id="header">` to identify the common header bar, a `<div id="content">` for the main page content, and <div id="footer"> for the footer content. These `div` elements with id attributes to indicate purpose, are now replaced with the HTML5 elements introduced below.

The `div` element is not obsolete, and is still commonly used, particularly to apply CSS to style particular content. However when an HTML5 structural element would fit the purpose of the `div`, the HTML5 element should be preferred over the use of a `div` with id.


## Entities
Special symbols that are generally *not* found on your keyboard, such as the copyright symbol, are created in HTML by special codes called __entities__.  There are many of these entities, but there are only a handful that are used commonly. It's a good idea to learn this short list and then know where to go to look up any others you might need later on.

Commonly used entities:

- &amp;copy; - copyright symbol - &copy;
- &amp;amp; - ampersand symbol - &amp;
- &amp;gt; - greater than symbol - >
- &amp;lt; - less than symbol - <

Note that you can usually type the ampersand, greater than, and less than symbols, but the entities are helpful when you are writing HTML for a technical site where you want HTML to show as text vs as browser rendered markup. (For example, to display the copyright entity in the list above, I wrote `&amp;copy;` to get the text "&amp;copy;" and avoid having the symbol itself display.)

{% include alert.html type="info"
    content="You will regularly be using `&copy;` to get the &copy; copyright symbol to put a copyright statement in the `footer` of your HTML pages for this class."
%}

For a full list of entities and their representations, see the [W3C Character Reference](https://dev.w3.org/html5/html-author/charref)

## Example Page
Here is an example HTML only page to show the use of the elements introduced so far.

{% gist mbMosman/1b74982faedfcc976a6bf014b1899850 basic-icecream.html %}

You can view this page on the web here: [HTML Only - Ice-Cream is Awesome!](https://htc-ccis1301.github.io/demo-ice-cream/html-only.html).  

When visiting the page above on the web, reduce the height of your browser window to about 1/2 your screen height, then click on the *in-page* links at the top of the page to see how they behave.

This example is similar to what will be expected for the Fan Page assignment.

## Note on Copyright
It's important to note that any text or graphic on a website is automatically copyrighted in the US regardless of there being a copyright mark on the web page. So be careful that you are not "stealing" other peoples work. Use the material of others only with permission and appropriate attribution to the author or creator.

If you use *any* content created by someone else, I will expect to see at a minimum an attribution in the footer of your page acknowledging the content creator. Using the work of others without permission and attribution breaks copyright law and is a type of plagiarism.

{% include alert.html type="danger"
    content="__Recall the statement on Academic Honesty in the Syllabus.__ For a first offense, you will get a warning in the feedback of your assignment. If this is done again, you will get no credit on the assignment. Repeated offenses will be reported to the college administration and may result in a 'F' or failing grade for the class."
%}

There can also be serious legal ramifications of using the copyrighted work of others. While their are some legal protections for "academic use", it is so much easier just to avoid the issue in the first place.  It is better to develop the habit of only using content that you have permission to use and appropriately credit the content owner or creator. You will see me doing this for content used on the course website and in examples, and I expect you to do the same thing.
