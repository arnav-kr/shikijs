# Shikijs
A JavaScript Library for Syntax Highlighting on the way with the themes you always wanted.

# Overview
`Shiki Highlighter JS` is a javascript library built on top of `Shikijs`. It provides more features than `Shikijs`. It is a Syntax Highlighting Library and Have Amazing themes. Its supports many languages for highlighting. Even the Code bits Yo're seeing in the documentation page is highlighted using `Shiki Highlighter JS`

#### Check Out [Available Themes](Themes.md) and [available Languages](Languages.md)


# Including the Library
To include the library to your project, add the following script element.
```html
<script src="https://cdn.jsdelivr.net/gh/arnav-kr/Shikijs/dist/V1.2.1/shikiHighlighter.min.js"></script>
```

# Getting Started
By default you get the Shiki object. We can perform different actions on this object.


# Methods

There are 4 different methods in `Shiki` object.

## `Shiki.getHTMLCode()`

|Argument Name|Type|Default|
|-------------|----|-------|
|code|String| - |
|language|String| - |
|theme|String| github-dark |

> **_NOTE:_**
> The third theme argument is optional as the default theme is `"github-dark"`


## `Shiki.highlight()`

`highlight()` comes in handy when you want to highligt code in an html element. It requires the reference of an html element as the argument, Shiki will replace it's textContent with the highlighted version of it.
It also requires to have certain attributes for the element. They are
|Name|Type|Required|
|----|----|--------|
|data-language|String|true|
data-theme|String|false|

_Example:_
**_HTML:_**
```html
<div id="myCode" data-language="py" data-theme="nord"></div>
```
**_JS_**
```javascript
var element = document.getElementById("myCode");
Shiki.highlight(element); //The text inside myCode div will automatically be highlighted
```


## `Shiki.highlightAll()`

`highlightAll()` comes in handy when you want to highligt code in a selection of html elements. It doesnt require any arguments to be passed with the function, Shiki will replace all the elements with the class `shiki-target` and replaces textContent with the highlighted version of it.
It also requires to have certain attributes for the all elements with the specific class. They are
|Name|Type|Required|
|----|----|--------|
|data-language|String|true|
data-theme|String|false|

_Example:_

**_HTML:_**
```html
<div class="shiki-target" data-language="py" data-theme="nord"></div>
<div class="shiki-target" data-language="js" data-theme="github-dark"></div>
<div class="shiki-target" data-language="c" data-theme="github-light"></div>
```
**_JS_**
```javascript
Shiki.highlightAll();
```

## `Shiki.setTheme()`

`setTheme()` allows you to change the default theme. It takes the name of the theme as argument and sets it as the default theme for the session.

```javascript
Shiki.setTheme("github-light");

Shiki.getHTMLCode("function start(){}", "javascript");
//The code returned would be highlighted in github-light
```


# Properties

## `Shiki.themes`

`themes` returns an array of all available themes you can use.

**_JS_**
```javascript
console.log(Shiki.themes);
```

## `Shiki.languages`

`languages` returns an array of all available languages you can use.

**_JS_**
```javascript
console.log(Shiki.languages);
```

## `Shiki.errorLog`

`errorLog` is an Array in which you can find all the errors that Shiki ran into when it was running or while it was highlighting your code. Every element of this array is an object. The object structure is as follows.

```javascript
{
  error:"ERROR_NAME",
  time:"ERROR_TIMESTAMP"
}
```


# At a Glance

By default you get the Shiki object. You can perform the below actions with it.

## Methods
| Name | Arguments| Argument Types | Return Type |
| --- | --- | --- | --- |
| Shiki.getHTMLCode() | Code, Language, Theme(optional) | String, String, String | Promise |
| Shiki.highlight() | HTML Element | HTMLElement | null |
| Shiki.highlightAll() | — | — | — |
| Shiki.setTheme() | Theme | String | — |

## Properties

| Name	| Type |
| --- | --- |
| Shiki.themes | Array |
| Shiki.languages | Array |
| Shiki.errorLog | Array |


_**Shiki Highlighter JS**_ by [Arnav Kumar](https://github/com/arnav-kr).

Having Trouble reading the documentation? view it [Online](https://arnav-kr.github.io/shikijs)


