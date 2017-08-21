---
title: "Web Standards & Architecture"
summary: "Before we begin developing for the web, it is important to understand how it works."
---


# {{ page.title }}
{{page.morea_summary}}

## Web Standards
The internet and the World Wide Web are public, open spaces. No one person or organization controls what is put out there.  However for content to be accessible to everyone, it is important that web architecture is standardized or this open network would be unable to operate smoothly.  

### The W3C
The [World Wide Web Consortium](https://www.w3c.org), or the W3C, is the main organization developing recommendations and prototype technologies for the Web. The W3C creates recommendations for web architecture, web browsers, web design & accessibility, and web services. These recommendations are created by *working groups* which are made up of people from various companies and organizations that research and develop web technologies.  These working groups put forward proposals which are then open for public review. After the review process the recommendations become web standards.

An example of a W3C Standard is the [HTML 5.1 Standard](https://www.w3.org/TR/2016/REC-html51-20161101/index.html#contents).  This is a *heavy* read, and I don't expect you to actually sit down and read the whole thing, but follow the link and check it out, just to get a sense of who is involved in these recommendations and what they look like.

The W3C also provides tools that help ensure that the web content that you write adheres to their standards. Throughout this course we will use W3C Validators for HTML & CSS to verify that our content meets their standards.

- [W3C HTML Validator](https://validator.w3.org/)
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

It's important to realize though that the W3C Standards are simply recommendations that people and organizations can choose either to follow or not. There is no one that actually enforces everyone to adhere to the standard. As we progress through this course, we will bump into things that we *should* do to address browsers that do not conform to the standard or *all* of the HTML5 Standard.

### Web Accessibility
An important consideration in web development is ensuring that the content we create is accessible by as many people as possible. The [Web Accessibility Initiative](http://www.w3.org/WAI), or WAI, is one of the W3C efforts. It's purpose is to develop and promote guidelines that remove barriers that might hinder access to Web content for those with physical, visual, auditory, or other disabilities.

> The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect. ~ Tim Berners-Lee, W3C Director and inventor of the World Wide Web.

The concept of [Universal Design](https://en.wikipedia.org/wiki/Universal_design) is growing quickly in Web development. It changes the focus away from techniques to accommodate a small population, and toward a design that benefits *everyone*, including those with disabilities. Universal Design aims to produce things that are aesthetically appealing and inherently usable to the greatest extent possible by everyone, regardless of their age, ability, or status in life.

### Standards and Law
There are several key standards and pieces of legislation to be aware of when it comes to the Web and accessibility:

- The WAI's [Web Content Accessiblity Guidelines (WCAG)](https://www.w3.org/WAI/WCAG20/glance/Overview), which aims to make content POUR - Perceivable, Operable, Understandable and Robust - in order to be usable by a universal audience.
- The American's with Disabilities Act (ADA), a federal law that requires business, federal, and state services - including Internet resources - are accessible to individuals with disabilities.
- Section 508 (of the Federal Rehabilitation Act), which has been amended to require US government agencies to provide comparable access to information technology that is comparable to the access available to others.

### Review Questions

- What is the W3C and why is it important?
- What is accessibility?  Why it is important?  
- What is universal design?  How is it different from accessibility?


## Web Architecture
As we learn to develop for the Web it is helpful to understand at least at a high-level, how the web works.

### HTML & HTTP
Two key words and technologies for this course are HTML & HTTP.  HTML stands for HyperText Markup Language.  It's a way to *markup* text so that a web browser can display it in a standard way.  HTTP stands for HyperText Transfer Protocol.  HTTP is the communication protocol that the browser uses to get information from the web.

{% include youtube-16x9.html  id="kBXQZMmiA4s"
    caption="Thanks to [Code.org](https://code.org) for sharing this video!"
%}

The video demonstrates how a web browser makes a request to get a resource from a web server. The Internet is an example of a client/server architecture, made up of many personal computers with web browser *clients*, and many web *servers* that use host the web pages and resources on the Web. I
t is important that you understand at a high-level the client/server architecture of the internet and how a web browser displays a web page. First, let's review how this client/server model works for a simple web request.

{% include img-medium.html url="/assets/images/intro-web-basics/webRequestResponse.png"
      alt="(Image showing the request-response cycle described below.)"
%}

1. The client (the web browser on your computer) begins by requesting a resource, such as index.html over HTTP.  This is sent as an HTTP request.
2. The web server locates the resource requested, ensuring that it is accessible by the client making the request.
3. The requested index.html file (or an error message if the file is not found or is not accessible to the client) is sent from the web server back to the client.  This is sent as an HTTP response.

{% include alert.html type="note"
    content="In this example, HTTP was used to request and send an HTML file, but many file types can be sent inside of an HTTP request, including image files, audio or video files, and various other text file formats such as PDF."
%}

An HTTP request and response are standardized message formats which provide information on who the information is sent from and to. This is much like sending a letter in an envelope through the mail with a return address and delivery address. It just uses a different sort of address called an IP address, which is discussed in more detail below.

In this class we will focus on the client side of the web, the web browser on your computer, as we focus on developing web pages that are displayed by the browser.  However in other classes you will explore the server side of the web, gaining a broader picture of web development.

### Network Protocols
The next video explains some of the various network protocols that allow the internet to function smoothly.  You will need to be able to identify these protocols and explain how they are used.   

{% include youtube-16x9.html  id="5o8CwafCxnU"
    caption="Thanks to [Code.org](https://code.org) for sharing this video!"
%}

### Review Questions

- What is a client/server architecture?  Explain how it is applied to the internet.
- Explain the process that takes place for your web browser to show you a page on the internet.
- What is HTTP? What is it used for?
- What can be done to make HTTP communications more private and secure?
- What is TCP/IP?
- Explain the relationship between IP addresses, domain names, and URIs/URLs.
- How does DNS Spoofing happen?


## Practice Quiz
This is a self-assessed, practice quiz to help you check your understanding of this material.  This quiz is not scored and can be taken as many times as you like to help review and check your understanding of the material presented.

{% include alert.html type="warning" content="There is also a graded quiz on D2L that is part of the weekly assignments. Do not confuse the two." %}

{% assign t_or_f = "True, False" | split: ', ' %}


{% assign q4_text = "Which of the following is a standards body that proactively develops recommendations and standards for the World Wide Web?" %}
{% assign q4_choices = "WCAG, Mosaic, TCP/IP, W3C" | split: ', ' %}

{% assign q4_feedbacks = "Sorry, that is not correct. This topic is covered in the textbook reading. | Sorry, that is not correct. This topic is covered in the textbook reading. | Sorry, that is not correct. This topic is covered in the textbook reading. | Correct! The W3C collects input from numerous sources to recommend and promote Web standards." | split: '| ' %}
{% include mc-quiz.html
   header="Question 1"
   text=q4_text
   choices=q4_choices
   answer=3
   feedback=q4_feedbacks
%}

{% assign q5_text = "The W3C promotes guidelines to support Web accessibility for individuals with disabilities." %}
{% assign q5_feedbacks = "Correct! The W3C promotes accessibility through their Web Accessibility Initiative (WAI) and the Web Content Accessibility Guidelines (WCAG). | Sorry. This is a false statement. This topic is covered in the textbook reading." | split: '| ' %}
{% include mc-quiz.html
   header="Question 2"
   text=q5_text
   choices=t_or_f
   answer=0
   feedback=q5_feedbacks
%}

{% assign q15_text = "The ADA is law that requires business and government services, including internet resources, to be accessible to people with disabilities." %}
{% assign q15_feedbacks = "Correct! ADA or Americans with Disabilities Act requires all business and government resources to be accessible to individuals with disabilities. | Sorry. This is a false statement. This topic is covered in the reading above. | split: '| ' %}
{% include mc-quiz.html
   header="Question 3"
   text=q15_text
   choices=t_or_f
   answer=0
   feedback=q15_feedbacks
%}

{% assign q6_text = "A network is made up of two or more computers that are connected to communicate and share resources." %}
{% assign q6_feedbacks = "Correct! |  Sorry. This is a true statement. This topic is covered in the video 'The Internet: IP Addresses & DNS'." | split: '| ' %}
{% include mc-quiz.html
   header="Question 4"
   text=q6_text
   choices=t_or_f
   answer=0
   feedback=q6_feedbacks
%}

{% assign q7_text = "A web browser acts as the server in the Client/Server model of the Web." %}
{% assign q7_feedbacks = "Sorry, this is a false statement. This topic is covered in the video 'The Internet: HTTP & HTML'. | Correct! A web browser acts as a client, not a server." | split: '| ' %}
{% include mc-quiz.html
   header="Question 5"
   text=q7_text
   choices=t_or_f
   answer=1
   feedback=q7_feedbacks
%}


{% assign q8_text = "Clients and servers communicate over the Internet by sending HTML requests and responses." %}
{% assign q8_feedbacks = "Sorry, this is a false statement. This topic is covered in the reading above and the video 'The Internet: HTTP & HTML'. | Correct!  HTML is the markup language used to build web pages. It is not a format for sending requests and responses between clients and servers." | split: '| ' %}
{% include mc-quiz.html
   header="Question 6"
   text=q8_text
   choices=t_or_f
   answer=1
   feedback=q8_feedbacks
%}

{% assign q1_text = "A protocol is a well-known set of rules and standards for to facilitate communication between computers on a network." %}
{% assign q1_feedbacks = "Correct! A protocol specifies rules for communication. | Sorry. This is a true statement.  This topic is covered in the video 'The Internet: IP Addresses & DNS'." | split: '| ' %}
{% include mc-quiz.html
   header="Question 7"
   text=q1_text
   choices=t_or_f
   answer=0
   feedback=q1_feedbacks
%}

{% assign q9_text = "HTTP is a protocol for exchanging many different types of files over the Web." %}
{% assign q9_feedbacks = "Correct! HTTP is typically used by web browsers for requesting resources from web servers. |  Sorry. This is a true statement. This topic is covered in the video "The Internet: HTTP & HTML"." | split: '| ' %}
{% include mc-quiz.html
   header="Question 8"
   text=q9_text
   choices=t_or_f
   answer=0
   feedback=q9_feedbacks
%}


{% assign q11_text = "A packet is a piece of a network message that also includes a sequence number and a checksum." %}
{% assign q9_feedbacks = "Correct! It also includes information on the sender and receiver. |  Sorry. This is a true statement. This topic is covered in the the video 'The Internet: IP Addresses & DNS'." | split: '| ' %}
{% include mc-quiz.html
   header="Question 9"
   text=q11_text
   choices=t_or_f
   answer=0
   feedback=q11_feedbacks
%}

{% assign q12_text = "What protocol specifies that messages will be broken into packets?" %}
{% assign q12_choices = "DNS, HTTP, TCP, WIPO" | split: ', ' %}

{% assign q12_feedbacks = "Sorry, DNS is not a communication protocol. This topic is covered in  the video 'The Internet: IP Addresses & DNS'. Try again. | Sorry, that is not correct. HTTP is a communication protocol, but not the correct one. This topic is covered in the video 'The Internet: IP Addresses & DNS'.  Try again. | Correct! TCP specifies that messages are broken into packets that include additional information to ensure the integrity of the communication. | Sorry, WIPO is not a communication protocol.  This topic is covered in  the video 'The Internet: IP Addresses & DNS'." | split: '| ' %}
{% include mc-quiz.html
   header="Question 10"
   text=q12_text
   choices=q12_choices
   answer=2
   feedback=q12_feedbacks
%}


{% assign q2_text = "Each device connected to the internet has a unique, numeric address called a(n) _______________." %}
{% assign q2_choices = "DNS, IP address, protocol address, POP account" | split: ', ' %}

{% assign q2_feedbacks = "Sorry, that is not correct. A DNS is a text-based URL, not a numeric address. This topic is covered in both the video 'The Internet: IP Addresses & DNS'. | Correct! Each internet connected device has a unique numeric IP Address. | Sorry, that is not correct. This topic is covered in the video 'The Internet: IP Addresses & DNS'. | Sorry, that is not correct. POP is a protocol used for email. This topic is covered in the video 'The Internet: IP Addresses & DNS'." | split: '| ' %}
{% include mc-quiz.html
   header="Question 11"
   text=q2_text
   choices=q2_choices
   answer=1
   feedback=q2_feedbacks
%}


{% assign q3_text = "The new IPv6 standard will double the number of IP addresses available for devices on the internet." %}
{% assign q3_feedbacks = "Sorry. This is a false statement as IPv6 will do much more than double the number of available addresses.  This topic is covered in the video 'The Internet: IP Addresses & DNS'. | Correct! IPv6 increases IP address length from 32 to 128 bits which does much more than double the number of addresses available." | split: '| ' %}
{% include mc-quiz.html
   header="Question 12"
   text=q3_text
   choices=t_or_f
   answer=1
   feedback=q3_feedbacks
%}


{% assign q14_text = "A domain name is a text based address for a device on the internet." %}
{% assign q14_feedbacks = "Correct! The text based domain name can be associated to a numeric IP address by using a DNS. | Sorry. This is a true statement. This topic is covered in the textbook reading." | split: '| ' %}
{% include mc-quiz.html
   header="Question 13"
   text=q14_text
   choices=t_or_f
   answer=0
   feedback=q14_feedbacks
%}
