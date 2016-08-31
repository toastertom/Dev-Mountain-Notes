# Day Four Notes
 Advanced HTML &amp; CSS

# HTML Attributes

* Syntax for **linking the CSS style sheet**. Note the only two attributes needed for the link to work are "rel" & "href". "link" is self closing.

```
<link rel="stylesheet" type="text/css" href="style.css"/>
```

* The **"a"** tag stands for anchor. It is used to create links on your page.

```
<a href="www.website.com">Link To Website</a>
```
* The **"img"** tag is used to embed images to your page. This tag is self closing so there is no need for closing brackets.

```
<img class="" src="image url">
```
* The **"span"** tag is used to group inline-elements in a document. The "span" tag provides no visual change by itself. The "span" tag provides a way to add a hook to a part of a text or a part of a document.

```
<span> </span>
```
* The **"alt"** attribute specifies an alternate text for an image, if the image cannot be displayed. The alt attribute provides alternative information for an image if a user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader). **This is required and makes the website more friendly to people with disabilities!**

```
<img class="" alt="image name" src="image url">
```
* The **"meta"** tag is used to describe your sight. I could also be used to contain images that will appear when someone shares a link to your sight. Note "meta" tags always go inside the "head" attribute.

```
<head>
<meta charset="UTF-8">
<meta name="description" content="Free Web tutorials">
<meta name="keywords" content="HTML,CSS,XML,JavaScript">
<meta name="author" content="Hege Refsnes">
</head>
```
* Use **"box-sizing: borderbox"** to make sure that a given box stays the perimeters that you gave it. Even when you add padding. The width and height properties include the content, the padding and border, but not the margin.

```
div {
    width: 300px;
    height: 100px;
    border: 1px solid blue;
    box-sizing: border-box;
}
```
# CSS

* **"Media Queries"** look at the capability of the device, and can be used to check many things, such as: width and height of the viewport. This allows you to set certain perimeters and designs to your website depending on the size of the users screen. Note these peramiters are set in CSS and the rules will be nested inside the media brackets like below.

```
@media screen and (max-width: 1000px) and (min-width: 700px) {
    ul li a:before {
        content: "Email: ";
        font-style: italic;
        color: #666666;
    }
}
```
