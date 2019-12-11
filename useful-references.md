# HTML

## HTML Elements Reference
For more information on HTML elements, see [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

## Accessibility with Headers
For people who are blind or visually impaired, screen reading software is used to parse through text on a web page. A common technique these folks will use to navigate the page is to jump from heading to heading to determine the overall content of the page more easily. That's why it's best practice to not skip one or more heading levels. If you did skip headings and went from <h1> to <h3>, you may cause confusion since the user has to deal with a missing heading. Don't bum out any of your users - structure your headings properly!

## Spans
The HTML `<span>` element is like a generic wrapper that is used to group text, mostly for styling purposes.
``` 
<style>
p {
  color: black;
}
.red {
  color: red;
}
</style>
<p>
  This sentence needs some <span class=”red”>visual emphasis</span> to really bring home the point.
</p>
```

## Attributes
Attributes provide additional information about an element, and are always specified in the start tag. Attributes usually come in name/value pairs like `name="value"`. e.g. An image’s alternative text (often a description for those with accessibility needs) is provided through the `alt` attribute.

## Self-Closing Tags
Because they don’t have a closing tag and consequently can’t contain anything inside them, self-enclosing elements usually carry a few attributes, to provide them with additional information.

Here are some examples:
* Line Break: <br /> 
* Image: <img />
* Form Input: <input />

## Links
The “HyperText” part of HTML defines what kind of links we use: hypertext links, a.k.a hyperlinks.
The `href` attribute (hypertext reference) is used to define the destination of the link.

3 types of destinations you can define:
* anchor targets, to navigate within the same page
* relative URLs, usually to navigate within the same website
* absolute URLs, usually to navigate to another website

You can also use additional attributes besides `a` and `href`:
* Specify the relationship between the current and linked document with the rel attribute
* Specify where to open the linked document with the target attribute

In the example below, we are setting the URL destination to The Labrador Club website, preventing this website from being able to access the window.opener property and ensuring it runs in a separate process with the noopener rel value. Finally we are requesting that the link open in a new window instead of the same one with the `_blank` target value.

```
<a href="https://thelabradorclub.com" rel="noopener" target="_blank"
  >Join The Labrador Retriever Club</a>
```

## Metadata
The `<head>` element contains the metadata for a web page.
Metadata is information about the page that isn’t displayed directly on the web page. Unlike the information inside of the `<body>` tag, the metadata in the head is information about the page itself.

### Title
A browser’s tab displays the title specified in the `<title>` tag. The `<title>` tag is always inside of the `<head>`.
```
<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journal</title>
  </head>
</html>
```

## Hierarchy
HTML is organized as a collection of family tree relationships. Understanding HTML hierarchy is important because child elements can inherit behavior and styling from their parent element.

## Semantic Elements
Structure elements allow you to organize the main parts of your page. They usually contain other HTML elements.

Here’s what a typical webpage could include:
* `<header>` as the first element of the page, that can include the logo and the tagline.
* `<nav>` as a list of links that go to the different pages of the website.
* `<h1>` as the title of the page.
* `<article>` as the main content of the page, like a blog post.
* `<footer>` as the last element of the page, located at the bottom.

![alt text](./resources/images/html-sectioning-elements.png "Positioning of Semantic HTML Elements")
