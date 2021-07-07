# Favicon 
A favicon is an icon that is used and redered on an HTML document. It is a diminutive for "favorite icon"<sup>1</sup>, and can be rendered by all web browsers, appering sometimes on the history and always on the top of the tab, following the title, for a visual reminder<sup>2</sup>. It is used to indicate that the user is on a specific page with a logo for example. Favicon uses the `.ico` or the `.png` and `.gif` extensions to presice that they are Favicons. These icons are used with *HTML* or *XHTML* in the `<head></head>` tag to be rendered by the browser. In this file system there is a favicon that you can look at. Here is a guide of usage of the favicon :

## Usage 
To use favicons, we have to know where to use them. Favicons are used in *HTML* or *XHTML* files. Inside these files, we use them a `<link/>` tag. Note that you can only use one Favicon per *HTML* or *XHTML* page. Now that the `<link/>` tag is defined inside the document, we have to make sure that the following favicon exists. If you want to create your own favicon, use https://www.favicon.cc to create it. Once created, use the following syntax to render your icon :
```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
```
###### Here *favicon.ico* represents the name of the `.ico` that you have created.

This is one method of using Favicons but others exist. Now to make your icon multiplatform, you can use a webmanifest, a file similar to json, used with the file name of `manifest.webmanifest`. Here is the syntax in `.jsonc` to use in your webmanifest to make your icon more acessible to others :

```jsonc
{
    // Project names etc
    "icons":[
        "src" : "(icon source here) : ./favicon.ico",
        "sizes":"(icon sizes here) : 16x16, 64x64",
        "type": "image/favicon"
    ]
    // Rest of the project
}
```

# Sources 
1. https://en.wikipedia.org/wiki/Favicon (consulted 7th of July 2021, 19:10 EST)
2. https://www.w3.org/2005/10/howto-favicon (consulted 7th of July 2021, 19:10 EST)
