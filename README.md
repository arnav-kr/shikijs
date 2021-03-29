# Shikijs
A JavaScript Library for Syntax Highlighting with Awesome themes

# Overview
`Shiki Highlighter JS` is a javascript library built on top of `Shikijs`. It provides more features than `Shikijs`. It is a Syntax Highlighting Library and Have Amazing themes. Its supports many languages for highlighting. Even the Code bits Yo're seeing in the documentation page is highlighted using `Shiki Highlighter JS`

# Including the Library
Add the following script to your site and shiki highlighter will be ready for use. 
```html
<script src="https://cdn.jsdelivr.net/gh/arnav-kr/Shikijs/dist/V1.2.1/shikiHighlighter.min.js"></script>
```


# Getting Started
So now we have included the script so we can now use shiki highlighter.

Here is a simple example of geting highlighted code and printing to the console.
```javascript
Shiki.getHTMLCode("function test(){}","javascript","github-dark")

.then(res => {

    console.log(res.code);//highlighted code

    console.log(res.language);//language of the code "javascript"

    console.log(res.theme);//theme of the code "github-dark"

});
``` 

Lets understand the code now.

`Shiki` is the main object of the library all the methods are available over this.
`.getHTMLCode(code,language,theme)` is a method of `Shiki` object which is used to get HTML highlighted code of the original one then you can just put the returned code in DOM. It returns a `Promise`.

# Methods

There are 4 methods in `Shiki` for use.

## `getHTMLCode()`

This method takes three arguments.
First argument is the String containing the `code` to highlight.
Second argument is the String containing the `language` of the code.
Third argument is the String containing the the name of `theme` you want to use.


> **_NOTE:_**

> The third theme argument is optional as the default `theme` is `"github-dark"`


## `highlight()`

`Shiki.highlight()` takes the reference of an HTML Element as the argument and highlights the code contents of that element. It is necessary for the element to have the `data-language=""` specifing the language of the code else it will not be highlighted. You can Specify the theme by `data-theme=""`


_Example:_


**_HTML:_**
```html
<div id="myCode" data-language="py" data-theme="nord"></div>
```

**_JS_**
```javscript
var element = document.getElementById("myCode");
Shiki.highlight(element); //The text inside myCode div will automatically be highlighted
```


## `highlightAll()`

`Shiki.highlightAll()` is an advanced form of `Shiki.highlight()`. It doesn't take any argument and highlights all element having `class="shiki-target"` which is required if you want to automatically highlight that element. `data-language=""` should also be present in the element.

## `setTheme()`

`Shiki.setTheme()` sets the theme for using. It takes the name of the theme as argument and sets it as the current theme.

# Properties

## `Shiki.themes`

`Shiki.themes` returns an Array of all available `themes` you can use.

## `Shiki.languages`

`Shiki.languages` returns an Array of all available `languages` you can use.

## `Shiki.errorLog`

`Shiki.errorLog` is an Array in which all the errors are stored that occur during highlighting your codes. Every error is stored as an object. The syntax of the error is as follows

```javascript
{
error:"The Error That Occured",
time:"The Time At Which the Error Occured"
}
```

# At a Glance

The main object is `Shiki` which containes all methods and properties.
A table explaining all is given below.


| Name	| Type | Arguments| Argument Types | Return Type |
| --- | --- | --- | --- | --- |
| Shiki.getHTMLCode() | Method | Code, Language, Theme(optional) | String, String, String | new Promise() |
| Shiki.highlight() | Method | HTML Element | HTMLElement | null |
| Shiki.highlightAll() | Method | — | — | — |
| Shiki.setTheme() | Method | Theme | String | — |
| Shiki.themes | Property | — | Array | — |
| Shiki.languages | Property | — | Array | — |
| Shiki.errorLog | Property | — | Array | — |





