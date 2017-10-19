---
title: "Media & Effects"
summary: "This module is focused on adding various types of media files (audio & video) to websites."
---

# {{ page.title }}
{{ page.summary }}

## Adding Media
Using media on your web pages can make them both more interesting and informative, but it is important to add them in a manner appropriate to your site.  The content should support the website's purpose. Also, remember that many visitors can be turned away by audio and video that plays automatically.  

 - [W3Schools: HTML Media](https://www.w3schools.com/html/html_media.asp)

### HTML5 Elements
We will focus on the new HTML5 elements for adding media.  However, when building pages for wide use, it is important to provide appropriate fallbacks for browsers that lack HTML5 support. Also note that there is currently no one *way* (encoding/file type) to get media on the web in a way supported by all browsers.  It is important to provide alternate file types and encodings as fallbacks in order to obtain broad support and accessibility across browsers.  

 - [W3Schools: HTML Video]( https://www.w3schools.com/html/html5_video.asp )
 - [W3Schools: HTML Audio]( https://www.w3schools.com/html/html5_audio.asp )
 - [SitePoint: HTML5 Video & Audio]( https://www.sitepoint.com/html5-video-and-audio-the-markup/ )

### Embed and iFrame
Elements can also be included into a page using the `embed` and `iframe` elements.  These elements can also be used inside of the HTML5 elements as a fallback.

The `embed` element has been used to add Adobe Flash (.swf file extension) to web pages, but it can also be used for adding video, audio, or other HTML including maps, Twitter feeds, etc. Many sites offer a button you can click on to get embed code for their services.
 - [W3Schools: Plugins (scroll down page to <embed>)]( https://www.w3schools.com/html/html_object.asp )
 - [Google Maps Help: Embed Google Map]( https://support.google.com/maps/answer/144361?co=GENIE.Platform%3DDesktop&hl=en )
 - [Embed Twitter](https://publish.twitter.com/)

 The `iframe` element has a long and complex history, but it is now most often to add content from other services to a web page. One common example is adding YouTube videos:
 - [W3Schools: iFrame for YouTube]( https://www.w3schools.com/html/html_youtube.asp )

### Accessibility
Just like with image media where it is important to provide alternate text for the image in the `alt` attribute, it is important to consider accessibility for other media types as well. With video, consider that some people may not be able to watch the video and provide text descriptions of the content where it is important.

For both video and audio files, consider that text alternatives are important for both those who physically cannot hear and those who may not want to have sound play for other reasons.  Provide captions on all video content and text transcripts for audio files.


## CSS Transform & Transition
We looked at the CSS `transform` property earlier to rotate images. However, you can use `transform` on any element, not just images. It can be used to alter text or other page elements as well. For example the `scale()` transform which affects the size of an element also applies to `font-size`, `padding`, `height`, and `width` of elements too.

 - [CSS Almanac: transform](https://css-tricks.com/almanac/properties/t/transform/)
 - [CSS Almanac: transform-origin](https://css-tricks.com/almanac/properties/t/transform-origin/)

The CSS `transition` properties can also be added to alter the display of items. They can be applied to color, background-color, border, font-size, font-weight, margin, padding, opacity and text-shadow.  These can be used in various ways to add interest and interactivity to your web pages.

 - [CSS Almanac: transition](https://css-tricks.com/almanac/properties/t/transition/)

## CSS Pseudo-classes
Link styles and CSS transitions are often applied using CSS *pseudo-classes*:

 - [CSS Almanac: :link](https://css-tricks.com/almanac/selectors/l/link/)
 - [CSS Almanac: :visited](http://css-tricks.com/almanac/selectors/v/visited/)
 - [CSS Almanac: :hover](https://css-tricks.com/almanac/selectors/h/hover/)
 - [CSS Almanac: :active](https://css-tricks.com/almanac/selectors/a/active/)

When using these pseudo-classes to style links, it is important to order your CSS rules in the order shown above so that they correctly override each other. To help you remember this order you might remember the phrase "Love Hate" abbreviated as LVHT to represent:
 - L (link)
 - V (visited)
 - H (hover)
 - A (active)

## Z-Index
When positioning items outside of normal page flow or using CSS `transform` or `transition`, it is sometimes important to consider how items overlay on a flat web page.  The CSS `z-index` allows us to send page elements in front of or behind other elements.

 - [CSS Almanac: z-index](https://css-tricks.com/almanac/properties/z/z-index/)


## CSS Dropdown Menu
CSS Dropdown menus are convenient choices for web navigation as they do not rely on having JavaScript enabled in the browser.  While many sites will use JavaScript or other framework components (i.e. Bootstrap) for navigation, this is a great demonstration of how basic CSS skills that you now know can be used to build interactive components for your web site.

 - [W3Schools: CSS Drowpdowns](https://www.w3schools.com/css/css_dropdowns.asp)
 - [CodePen: Simple Pure CSS Drop Down Meun by Phil Hoyt](https://codepen.io/philhoyt/pen/ujHzd?editors=1100#0)

## Review Questions

 - What are some reasons that audio or video you test and see working fine may not work for other visitors to your site?
 - What is the embed element used for?
 - How do you use the new HTML5 audio and video elements to add audio and video to your page?
 - What are some fallback options for browsers that do not support HTML5?
 - What is the iframe element used for?
 - How can you use CSS to rotate an element on your web page?
 - How can you use CSS to double an element's size?
 - How can you use the CSS transition property to gradually increase an element's font-size?
 - How can you have links that have previously been clicked on display in a different color?
 - How could you have a link color change when a person hovers over the link?
 - How could you have a button change color when someone hovers over it?
