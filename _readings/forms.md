---
title: "Building & Styling Forms"
summary: "This modules is focused on building web forms.  Forms are commonly used on many sites to collect data."
---

# {{ page.title }}
{{ page.summary }}

## Basic form structure
A web form is created using the `<form>` element and contains labels, inputs and buttons.

The form element must include an `action` which indicates the URL for where the form information should be submitted.  The `method` indicates how the data is sent to the web server - `get` or `post`.  The `get` method is the default and causes the data to be appended to the URL that is sent to the web server.  This makes the data sent rather public as it is visible on the request URL.  The alternate method of `post` is more private as the information is transmitted in the body of the message, not on the URL.  This is method is generally preferred.  The form element also allows for an optional `name` and/or `id` which can help provide access to the form for client-side validation of the information using JavaScript.

 - [W3Schools: HTML Forms]( https://www.w3schools.com/html/html_forms.asp )


### Form Controls
There are a variety of form input controls that can be used on a web form.

 - [W3Schools: Form Elements](https://www.w3schools.com/html/html_form_elements.asp)
 - [W3Schools: Input Types](https://www.w3schools.com/html/html_form_input_types.asp)
 - [W3Schools: Input Attributes](https://www.w3schools.com/html/html_form_attributes.asp)

Pay particular attention to the following basic controls:

- Text Box
- Submit & Reset Buttons
- Check Box and Radio Button
- Hidden Field and Password Box
- Text Area
- Select List

and the following newer HTML5 Controls:

- Email & Telephone
- Datalist
- Slider and Spinner
- Calendar
- Color Well

A form fields can be required using the HTML5 `required` attribute, however it is important to remember that it is only checked by browsers that support HTML5.  

It is also good to remember that any type of client-side form validation can be circumvented fairly easily, so as you work with back-end services to handle this data, any browser validation should be repeated on the server.  Client-side validation should be treated as merely a convenience to speed up validation for the user, and not relied upon for clean and valid input data.

### Accessibility
Make sure to use one of the two accepted methods to associate a form control with a label to support accessibility tools.

1. Use the label as a container around both the text description and the form control.
2. Use the label as a container for only the text description and then use the `for` attribute on the label element to associate it with the `id` attribute of the form control.

The second method is generally preferred as it allows more flexibility in the form design.

## Styling Forms
There isn't anything particularly special to note about styling web forms. Just use an appropriate selector for the element and add CSS for margin/padding, text, color, or whatever it is you need or desire to make the form look nice. However it is very helpful to consider how your form will look and behave on a mobile device versus a computer. Where there is a larger display, putting labels next to input fields is helpful.  However on mobile devices these are generally better placed "stacked" or with the label above the input field allowing the full width of the display for the input area.


## Review Questions

 - What is the purpose of an HTML form?  
 - What attribute(s) are required on the form element?
 - What is the purpose of the `method` attribute?
 - What is the difference between the `get` and `post` method of form submission?
 - Which is considered more private?  
 - How do you indicate a form field is required before the form can be submitted?
 - Does requiring a field provide a 100% guarantee that the data is actually present?
 - What are the two methods used to associate descriptive text to form controls?
