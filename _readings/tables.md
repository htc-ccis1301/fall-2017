---
title: "Building & Styling Tables"
summary: "This modules is focused on structuring and styling tables for the web.  Tables are a common feature on web pages, organizing information to make it easier to read and understand."
---

# {{ page.title }}
{{ page.summary }}

## Overview
Tables can organize information, making it easier to read and understand.  With the addition of some JavaScript (not covered in this course), the data can also sorted and filtered.  This can allow data that was once printed and distributed as reports, or emailed out in spreadsheets to be accessible on the web any time and anywhere.  


## Basic Table Structure
{% include alert.html type="warning"
   content="The example tables below are styled with the CSS for this site, so they will look different without CSS applied."
%}

A basic table `<table>` is just made of rows `<tr>` and cells `<td>` (which make up the columns).

{% gist 5785c6e9534e956b79d7 basicTable.html %}

That produces a table that is structured like this:
<table class="style: margin: 10px; padding: 5px;">
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 2</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 3</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 2</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 3</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 2</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 3</td>
    </tr>
</table>


### Headings and Caption
To make the table a little fancier, you can also add headings and a caption or title.

{% gist 5785c6e9534e956b79d7 basicTable2.html %}

That produces a table that is structured like this:
<table class="style: margin: 10px; padding: 5px;">
    <caption>Basic Table with Headings</caption>
    <tr>
        <th style="padding: 5px; border: 1px solid #000066;">Heading 1</th>
        <th style="padding: 5px; border: 1px solid #000066;">Heading 2</th>
        <th style="padding: 5px; border: 1px solid #000066;">Heading 3</th>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 2</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 3</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 2</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 3</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 2</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 3</td>
    </tr>
</table>


### Spanning Rows & Columns
It's not uncommon to want a row or column to take up the space of more than one *cell*.  This can improve the table display when there are things like grouped rows or columns. This is not something used for every table, but it is important to know that you *can* do this.

{% gist 5785c6e9534e956b79d7 basicTable3.html %}

That produces a table that is structured like this:
<table class="style: margin: 10px; padding: 5px;">
    <caption>Table Spanning Rows & Columns</caption>
    <tr>
        <th style="padding: 5px; border: 1px solid #000066;">Heading 1</th>
        <th style="padding: 5px; border: 1px solid #000066;" colspan="2">Heading 2</th>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 2 part 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 1, Column 2 part 2</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 2, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;" colspan="2">Row 2, Column 2 spanning columns</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 2 part 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 3, Column 2 part 2</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;" rowspan="2">Row 4, Column 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 4, Column 2 part 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 4, Column 3 part 1</td>
    </tr>
    <tr>
        <td style="padding: 5px; border: 1px solid #000066;">Row 4, Column 2 part 1</td>
        <td style="padding: 5px; border: 1px solid #000066;">Row 4, Column 3 part 1</td>
    </tr>
</table>


### Accessibility
The `id` and `headers` attributes can be used in your tables to support accessibility:

 - [W3Schools: HTML <td> headers Attribute](https://www.w3schools.com/tags/att_td_headers.asp)


### Table Structure
Tables can get rather complex, especially if they are containing groups of data with summary information.  To assist with the layout of these tables, there are grouping elements to help you structure your tables.  These elements are `thead`, `tbody` and `tfoot`.  While it is not necessary to use all of these in every table, they are often used to separate headers from the table body or contents, and if the table contains summary information, it should be placed in the `tfoot`.

 - [W3Schools: HTML <thead> Tag](https://www.w3schools.com/tags/tag_thead.asp)
 - [W3Schools: HTML <tbody> Tag](https://www.w3schools.com/tags/tag_tbody.asp)
 - [W3Schools: HTML <tfoot> Tag](https://www.w3schools.com/tags/tag_tfoot.asp)


## Styling Tables
Older HTML tables were styled using attributes on the HTML tag.  Now that CSS is widely supported, it is considered a best practice to avoid the use of the HTML attributes for styling and to use CSS instead.  

The tables above are styled using the following CSS:
<pre>
table {
  margin: 10px;
  padding: 5px;
}

th,td {
  padding: 5px;
  border: 1px solid #000066;
}
</pre>

### Styling table rows
It's often desirable to alternate the background color on every other table row for readability.  This can be done using CSS structural pseudoclasses.

 - [CSS Almanac: :first-of-type]( https://css-tricks.com/almanac/selectors/f/first-of-type/ )
 - [CSS Almanac: :nth-of-type]( https://css-tricks.com/almanac/selectors/n/nth-of-type/ )
 - [CSS Almanac: :last-of-type]( https://css-tricks.com/almanac/selectors/l/last-of-type/ )


## Additional Resources
More information can be found on the following pages:

 - [W3C Schools: HTML Tables]( https://www.w3schools.com/html/html_tables.asp )
 - [W3C Schools: CSS Tables]( https://www.w3schools.com/css/css_table.asp )
 - [CSS Tricks: A Complete Guide to Tables]( https://css-tricks.com/complete-guide-table-element/ )
 - [Mozilla: HTML Table Element Reference]( https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table )


## Review Questions

 - What is the purpose of a table in HTML?  
 - Why should you not use attributes such as `cellpadding`, `cellspacing`, and `summary` on new HTML pages?
 - What is the difference between a `th` and a `td` element?
 - Where is a table caption positioned in the table HTML?  Why it is used?
 - How do you have a table cell span multiple rows?  Multiple columns?
 - How is the `headers` attribute used in an HTML table?  Why is it used?
 - How do you eliminate the space between the table's cell borders using CSS?
 - How do you style table rows so that every other row has a different background color?
 - Tables have 3 structural elements to group rows.  One is `tbody`, what are the other two? Give an example of how they might be used.
