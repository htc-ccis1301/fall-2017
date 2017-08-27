---
title: "HTML Document Structure"
summary: "An introduction to the DOM, which stands for Document Object Model, and the tree-like structure it gives to an HTML page."
---

# {{ page.title }}
{{page.morea_summary}}

## HTML Template
We will use this basic HTML5 template in our discussion of the DOM - Document Object Model - structure that follows.

{% gist mbMosman/5785c6e9534e956b79d7 basicHTML5.html %}


## HTML Structure
It is important to understand that the structure of HTML is like a tree. It is a hierarchical branching structure - much like a family tree or a file system's folder structure. This structure is called the DOM (Document Object Model), and it is used by web browsers to interpret the structure of a web page in order to *render*, or display it.

The `html` element is the root of this structure. Looking at our template it has two children - `head` and `body`.  These children are between (or inside) the opening and closing tags of the element. You could also say they are *wrapped* (or surrounded) by the `<html>` tag.  Because the `head` and `body` have the same parent element, they are siblings.

Using the Chrome Browser Developer tools, we can view the structure of the HTML document in an interactive way that allows elements to be expanded and collapsed.  
<img src="{{ "/assets/images/intro-dom/basic-html-tree1.png" | prepend:site.baseurl }}"
    alt="Image illustrating the collapsed tree structure of the template above. The html element contains the head and body.">

By clicking the arrow next to an element name, you can see what is inside of it.  
<img src="{{ "/assets/images/intro-dom/basic-html-tree2.png" | prepend:site.baseurl }}"
    alt="Image illustrating the expanded tree structure of the template above. The html element contains the head and body, and the head is expanded showing its children.">

You might be wondering, "What about that `<!DOCTYPE html>`?" After all it comes first so why isn't it the root of the DOM? The `DOCTYPE` is a special markup tag that is informational. That's why it has the `!` at the beginning. We discuss the `DOCTYPE` further in the Reading: [HTML Template Explained](/intro-template-html.html). For now, just know that it is not considered part of the DOM structure. That's why it's greyed out in the Developer Tools view shown in the images above.

### Attributes
Some HTML elements contain one or more attributes. An __attribute__ is a key-value pair that follows the name of the element inside the opening HTML tag. The name of the attribute is on the left side of the equal sign (=) and the value is on the right.

In the example template the `html` element has a `lang` attribute with the value of "en".  
{% highlight html %}
<html lang="en">
{% endhighlight %}

It is required to always put the value of an attribute in quotes.

{% assign q1_text = "How many attributes does the `link` element have?" %}
{% assign q1_feedbacks = "Look at the `link` element carefully.  An attribute is a name=value pairing. | Look at the `link` element carefully.  An attribute is a name=value pairing. | Correct!  The `link` element has two attributes: `rel` and `href`. | Look at the `link` element carefully.  An attribute is a name=value pairing." | split: '| ' %}
{% assign q1_choices = " 0 | 1 | 2 | 3 " | split: '|' %}
{% include mc-quiz.html
  header="Question 1"
  answer=2
  text=q1_text
  choices=q1_choices
  feedback=q1_feedbacks
%}

{% assign q2_text = "Is `utf-8` the name of an attribute or an attribute value?" %}
{% assign q2_feedbacks = "Look at the `meta` element carefully.  An attribute is a name=value pairing, with the name on the left and the value on the right. | Correct!  The `meta` element has a `charset` attribute with the value `utf-8`." | split: '| ' %}
{% assign q2_choices = " name | value " | split: '|' %}
{% include mc-quiz.html
  header="Question 2"
  answer=1
  text=q2_text
  choices=q2_choices
  feedback=q2_feedbacks
%}


### Parents & Children
The relationship of parent-child only applies if one element is directly contained inside of the other.  As mentioned above, the `head` element is a child of the `html` element.  However the `title` element is *not* a child of `html`.  It is a *child* of `head`, not `html`.  However it may also be considered a *descendant* of the `html` element.

Using the HTML template shown in the Basic HTML5 Template Gist above, answer the following questions.
{% assign q1-text = "The `body` element is a child of the `html` element." %}
{% assign q1-choices = "True | False" | split: '|' %}
{% assign q1_feedbacks = "Correct!  It is directly contained in the `html` element. | Look at the structure carefully.  When one element is directly contained inside the open and closing tag of another, it is considered a child." | split: '|' %}
{% include mc-quiz.html header="Question 1" answer=0 text=q1-text choices=q1-choices feedback=q1_feedbacks %}

{% assign q2-text = "The `meta` element is a child of the `html` element." %}
{% assign q2-choices = "True | False" | split: '|' %}
{% assign q2_feedbacks = "Look at the structure carefully.  When one element is directly contained inside the open and closing tag of another, it is considered a child. | Correct!  Because the `meta` element is not directly contained in the `html` element, it is not considered a child." | split: '| ' %}
{% include mc-quiz.html header="Question 2" answer=1 text=q2-text choices=q2-choices feedback=q2_feedbacks %}

{% assign q3-text = "The `p` element is a descendant of the `html` element." %}
{% assign q3-choices = "True | False" | split: '|' %}
{% assign q3_feedbacks = "Correct!  Because the `p` element is contained between the opening and closing tags of the `html` element, it is a descendant. However it is not considered a child because it is directly inside of the `body` element not `html`. | Look at the structure carefully.  When one element is contained inside the open and closing tag of another, it is a descendant of that element. The descendant relationship is more broad and inclusive than parent-child." | split: '| ' %}
{% include mc-quiz.html header="Question 3" answer=0 text=q3-text choices=q3-choices feedback=q3_feedbacks %}


### Siblings
When two elements have the same parent (when they are both directly contained by the same opening and closing tags) they are siblings to each other.  As mentioned above, both the `head` and `body` elements are children of the `html` element, so they are siblings.

Using the HTML template shown in the Basic HTML5 Template Gist above, answer the following questions.
{% assign q1-text = "The `title` is a sibling of the `head` element." %}
{% assign q1-choices = "True | False" | split: '|' %}
{% assign q1_feedbacks = "Look at the structure carefully and identify the parent of each element to see if it is the same. | Correct!  They are not siblings because they have different parents." | split: '|' %}
{% include mc-quiz.html header="Question 1" answer=1 text=q1-text choices=q1-choices feedback=q1_feedbacks %}

{% assign q2-text = "The `title` is a sibling of the `meta` element." %}
{% assign q2-choices = "True | False" | split: '|' %}
{% assign q2_feedbacks = "Correct!  They have the same parent element, `head`. | Look at the structure carefully and identify the parent of `title` and `meta` to see if it is the same." | split: '|' %}
{% include mc-quiz.html header="Question 2" answer=0 text=q2-text choices=q2-choices feedback=q2_feedbacks %}

### Summary
As you are looking at these relationships, be careful that you do not just rely on spacing or indentation, as that is sometimes incorrect or missing entirely from an HTML document. If you are not careful, it can be easy to mistake the parent/child relationship for a sibling relationship.  __Pay close attention to the closing tags of the elements.__  

- In a sibling relationship the closing tag of the first element comes *before* the opening tag of the second element.
- In a parent/child relationship the closing tag of the parent element comes *after* both the opening and closing tag of the child element.

## Test your Skills
Walk through the HTML for the basic HTML5 template above and for each element, identify:

- What is the element's parent?
- What are the element's siblings?
- Does it have any children? If so, what are its child elements?

Be aware that some elements are both a parent and a child - the `head` for example. This shouldn't seem strange to you as it happens often in our families. My mother is a *parent* to both my brother and I, but she is also a *child* of her own parents, my grandparents. When discussing DOM relationships it is important to identify both elements to make the relationship clear.


## Practice Quiz

{% assign num_choices = " 0 | 1 | 2 | 3 " | split: '|' %}
{% assign dom_choices = " the parent | a child | a sibling | no relation " | split: '|' %}

{% assign q_text = "How many child elements does the `html` element have?" %}
{% assign q_feedbacks = "Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element. | Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element. | Correct!  The `head` and the `body` elements are its children. | Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element." | split: '| ' %}
{% include mc-quiz.html
  header="Question 1"
  answer=2
  text=q_text
  choices=num_choices
  feedback=q_feedbacks
%}

{% assign q_text = "The `html` element is ____________ to the `body` element." %}
{% assign q_feedbacks = "Correct!  Because both the opening and closing tags for the `body` are between the opening and closing `html` tag, the `html` element is a parent of the (child) `body`. | Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element. | Look at the structure carefully.  When two tags have the same parent element, they are siblings. | Look at the structure more carefully.  When one HTML tag is contained inside the open and closing tag of another, the outer element is a parent and the inner is its child. When two elements have the same parent, the two elements are siblings." | split: '| ' %}
{% include mc-quiz.html
  header="Question 2"
  answer=0
  text=q_text
  choices=dom_choices
  feedback=q_feedbacks
%}

{% assign q_text = "How many child elements does the `body` element have?" %}
{% assign q_feedbacks = "Look at the structure carefully.  When one HTML element is contained inside the open and closing tag of another, it is considered a child element. | Correct!  The `p` element is the one and only child of the `body`. |  Look at the structure carefully.  When one HTML element is contained inside the open and closing tag of another, it is considered a child element. |  Look at the structure carefully.  When one HTML element is contained inside the open and closing tag of another, it is considered a child element. " | split: '| ' %}
{% include mc-quiz.html
  header="Question 3"
  answer=1
  text=q_text
  choices=num_choices
  feedback=q_feedbacks
%}

{% assign q_text = "The `head` element is ____________ to the `body` element." %}
{% assign q_feedbacks = "Look at the structure carefully.  When one HTML element directly contains another, it is considered a parent element. | Look at the structure carefully.  When one HTML element is contained inside the open and closing tag of another, it is considered a child element. | Correct!  Because the `head` and the `body` are both children of the `html` element, the `head` element is a sibling of the `body` element. | Look at the structure more carefully.  When one HTML element is contained inside the open and closing tag of another, the outer element is a parent and the inner is its child. When two elements have the same parent, the two elements are siblings." | split: '| ' %}
{% include mc-quiz.html
  header="Question 4"
  answer=2
  text=q_text
  choices=dom_choices
  feedback=q_feedbacks
%}

{% assign q_text = "How many child elements does the `title` element have?" %}
{% assign q_feedbacks = "Correct!  Because the text is not considered an HTML *element*. | Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element. Is there another HTML element in the `title`? | Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element. | Look at the structure carefully.  When one HTML tag is contained inside the open and closing tag of another, it is considered a child element." | split: '| ' %}
{% include mc-quiz.html
  header="Question 5"
  answer=0
  text=q_text
  choices=num_choices
  feedback=q_feedbacks
%}

{% assign q_text = "How many sibling elements does the `title` element have?" %}
{% assign q_feedbacks = "Look at the structure carefully.  When two elements have the same parent, the two elements are siblings. | Correct! The `title` and `meta` elements are siblings because they both have the `head` as their parent. | Look at the structure carefully. When two elements have the same parent, the two elements are siblings. | Look at the structure carefully.  When two elements have the same parent, the two elements are siblings." | split: '| ' %}
{% include mc-quiz.html
  header="Question 6"
  answer=1
  text=q_text
  choices=num_choices
  feedback=q_feedbacks
%}

{% assign q_text = "The `title` element is ____________ to the `body` element." %}
{% assign q_feedbacks = "Look at the structure carefully.  When one HTML element directly contains another, it is considered a parent element. | Look at the structure carefully.  When one HTML element is contained inside the open and closing tag of another, it is considered a child element. | Look at the structure more carefully. When two elements have the same parent, the two elements are siblings. | Correct!  There is no parent/child relationship between the `title` and `body`, and they also do not have the same parent element so they are not siblings. That means there is no relationship between them." | split: '| ' %}
{% include mc-quiz.html
  header="Question 7"
  answer=3
  text=q_text
  choices=dom_choices
  feedback=q_feedbacks
%}

{% assign q_text = "Which of the following is an attribute?" %}
{% assign q_choices = " html | lang | head | meta " | split: '|' %}
{% assign q_feedbacks = "The `html` element *has* an attribute, but it is an element not an attribute. | Correct, `lang` is the attribute on the `html` element. It's value is `en`. | Sorry, `head` is an element, not an attribute. | The `meta` element *has* an attribute, but it is an element not an attribute." | split: '| ' %}
{% include mc-quiz.html
  header="Question 8"
  answer=1
  text=q_text
  choices=q_choices
  feedback=q_feedbacks
%}
