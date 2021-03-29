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
    

