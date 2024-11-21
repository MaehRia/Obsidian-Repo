### A Simple HTML document

Here are given an example of a simple HTML document and a link to a documentation that provides information about [creating web page with Notepad or TextEdit](https://www.w3schools.com/html/html_editors.asp).

Shortcut: "!" + Tab
``` html
<!DOCTYPE html>
<html>

<head>
<title>Page Title</title>
</head>

<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>

</html>
```

Explanation:

- The `<!DOCTYPE html>` declaration defines that this document is an HTML5 document. All HTML documents must start with that document type declaration. It must only appear once, at the top of the page (before any HTML tags).
  
- The `<html>` element is the root element of an HTML page. The HTML document itself begins with `<html>` and ends with `</html>`.
  
- The `<head>` element contains meta information about the HTML page.(more detailed explanation is given below)

- The `<title>` element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab).
  
- The visible part of the HTML document is between `<body>` and `</body>`. The `<body>` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
  
- The `<h1>` element defines a large heading.
  
- The `<p>` element defines a paragraph.

### About the \<head> element and metadata (meta information)

>The HTML `<head>` element is a container for the following elements: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, and `<base>`.
>
>The `<head>` element is a container for metadata (data about data) and is placed between the `<html>` tag and the `<body>` tag.
>
>HTML metadata is data about the HTML document. Metadata is not displayed.
>
>Metadata typically define the document title, character set, styles, scripts, and other meta information.



### What is an HTML element?

An HTML element is defined by a start tag, some content, and an end tag:

\<tagname> Content goes here... \</tagname>

Such are the 8th and 9th lines in code above.

| Start tag | Element content       | End tag   |
| --------- | --------------------- | --------- |
| `<h1>`    | My First Heading      | `</h1>`   |
| `<p>`     | My first paragraph.   | `</p>`    |
| `<br>`    | none                  | none      |

### Empty Element `<br>`

HTML elements with no content are called empty elements.

The `<br>` tag defines a line break, and is an empty element without a closing tag:

```html
<p>This is a <br> paragraph with a line break.</p>
```


### Web Browsers

The purpose of a web browser (Chrome, Edge, Firefox, Safari) is to read HTML documents and display them correctly. A browser does not display the HTML tags, but uses them to determine how to display the document.

### HTML page structure

Below is a visualization of an HTML page structure:

![[Pasted image 20240925231825.png]]

### HTML Headings

HTML headings are defined with the `<h1>` to `<h6>` tags.

### HTML Paragraphs

TML paragraphs are defined with the `<p>` tag.

### HTML Links

HTML links are defined with the \<a> tag.

```html
<a href="https://www.w3schools.com">This is a link</a>
```

The link's destination is specified in the `href` attribute. 

> [!attention] 
> Attributes are used to provide additional information about HTML elements. 

### HTML Images

HTML images are defined with the `<img>` tag.

The source file (`src`), alternative text (`alt`), `width`, and `height`
are provided as attributes:

```html
<img src="w3schools.jpg" alt="W3Schools.com" width="104" height="142">
```

### HTML attributes

HTML attributes provide additional information about HTML elements.

- All HTML elements can have attributes,
- Attributes provide additional information about elements.
- Attributes are always specified in the start tag
- Attributes always come in name-value pairs like: name="value"

### The href attribute

The `<a>` tag defines a hyperlink. The `href` attribute specifies the URL of the page the link goes to: 

```html
<a href="https://www.lanadelrey.com/">The Bible's official page</a>
```



### Table

```html
<table>

<tr>
<th>Name</th>
<th>Surname</th>
<th>Age</th>
<th>Gender</th>
</tr>

<tr>
<td>Ramzan</td>
<td>Kadyrov</td>
<td>38</td>
<td>Male</td>
</tr>

<tr>
<td>Hayk</td>
<td>Hakobyan</td>
<td>16</td>
<td>Male</td>
</tr>

<tr>
<td>Anna</td>
<td>Lebedko</td>
<td>25</td>
<td>Female</td>
</tr>
</table>
```


```html
<table>
<tr>
<th colspan="4">Name Surname Age Gender</th>
</tr>

<td rowspan="2">Male</td>
</table>
```


```css
table, th, tr, td{
	border: 2px solid black;
	border-collapse:collapse;
}
```


```html
<marquee direction="right" width="700 px" height="100 px" bgcolor="pink" scrollamount="10" loop="5">Born to Die</marquee>
```