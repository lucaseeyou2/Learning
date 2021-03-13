# Markdown guide

###### *inspired by this cheatsheet : https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet*, by Adam Prichard, Github

# Introduction
Markdown is a file extension made to convert text to HTML or XHTML. It has the goal of informing when named Readme or info with the extension md and is widely used in coding. It is a fairly lightweight language, designed to be easy to read, with multiple simple functions. Markdown can also be used with *HTML* but with not all of it's functionalities. This is a guide that will cover the entirety Markdown, with all off it's content, so lets get started. Before starting to create a file, make sure that it has the extension of markdown which is `.md` or `.markdown`.

## Headers 
A header is whats on the top of a page, indicating a title. Headers in Markdown aren't necessarily at the top of a page, but they can serve of sub-titles to introduce paragraphs, or be used in writting, because some are larger than others. In Markdown we express these headers in form of `#`. These headers are quite similar to the HTML versions (`<h1>` for example), and have the same role. Here are some headers : 
```md
syntax is as : 
`(nth importance number of #) text`
# Header of first importance
## Header of second importance
### Header of third importance
#### Header of fourth importance 
##### Header of fifth importance
###### Header of sixth importance
```
that will result in :
# Header of first importance
## Header of second importance
### Header of third importance
#### Header of fourth importance 
##### Header of fifth importance
###### Header of sixth importance
 
Though this is the most commonly used syntax for headers, other styles of headers can be used in Markdown to express an equivalent statement but with a different writting. Thought these are different writtings, they arent't for all the headers mentionned before because they only apply to headers of first and second importance (`h1` and `h2` in *HTML*). Here is an example of headers that aren't usualy with the `#` syntax: 
```md 
`syntax is as :`
`text`
`=== or ---`
different h1
===
different h2
---
```

Will result in : 

different h1
===
different h2
---
## Emphasis
Emphasis are styles applied to text to make them more important or with certain styles. These different styles are numerous, and all of them can be combined. To list them all there is *italics*, **bolds** and ~~strikthrough~~ text. Here is a table with all of the possible emphasis styles in Markdown code that you can apply when writting a Markdown file :
| bold                             | Italic                           | strikethrough                                |
| ----                             | ------                           | -------------------                          |
| `**bold text**`                  | `*italic text*`                  | `~~strikethrought text~~`                    |
| `__text__`                       | `_italic text_`                  |                                              |
| `**_bold and italic_**`          | `_**italic and bold**_`          | `**~~strikethrough and bold~~**`             |
| `___bold and italic___`          | `___italic and bold___`          | `__~~strikethrough and bold~~__`             |
| `**~~bold and strikethrough**~~` | `~~*italic and strikethrough*~~` | `_~~strikethrough and italic~~_`             |
| `__~~bold and strikethrough~~__` | `_~~italic and strikethrough~~_` | `___~~strikethrough and italic and bold~~___`|

###### ps: there may be more but position and character choice doesn't change anything here
## Lists 
List are useful in Markdown, when it is to list the caracteristics of your project or listing the steps of an installation, such examples can use lists. Like in *HTML*, lists are separated in two groups : ordered lists and unordered list (`<ol></ol>` and `<ul></ul>` in *HTML*). Here is an example of two markdown lists : 
```md 
ordered list :
syntax : number, listed item 
1. eggs 
2. wheat
3. flour
4. cream
```
This will return : 
1. eggs 
2. wheat
3. flour
4. cream
###### Remember to order your items, if not, they won't be rendered as lists but text. 
```md
unordered list :
syntax : `(symbols *, -, or +), listed item`

- You can use hyphens to list an item 
* Asterixes can also be used to list
+ Unusual one but pluses as well !
```
This will return :
- You can use hyphens to list an item 
* Asterixes can also be used to list
+ Unusual one but pluses as well !
```md 
- something
  * child of the element
  1. ordered of the first
  2. same branch lol
      * child of the first 
        1. same level :)
        2. same as the first
            * child of second
            1. yeah 
            2. same 
```
Returns :
- something
  * child of the element
  1. ordered of the first
  2. same branch lol
      * child of the first 
        1. same level :)
==            * child of second
            1. yeah 
            2. same 

Here this example demonstrates lists and their different behaviours. Let's talk about ordered lists first. On the normal level, their markers are different. I will use CSS to explain this part. On a default level, the tokens are under decimal forms, like 1, 2, 3 (`list-style-type: decimal;` in css) etc. Then on the first lower level, the tokens are in lower roman (`list-style-type: lower-roman;` in css), like i, ii, iii, iv, v etc. Delving again to deeper levels, we get alphanumeric tokens (`list-style-type: lower-alpha;`), like a, b, c, d etc. And it stays 

Now let's talk about the unordered lists. Lists like those, have similar tokens, but with no numeration. On the first level, the token will be a dot (in css `list-style-type: disc;`). On the second level, it will be a hollow circle (in css `list-style-type: dot;`). The on the third, the token will become a square (`list-style-type: square;`). 

## Code 
Code is something that is important to Markdown files because they can indicate how to use a certain function or block of code. Code can be expressed in multiple manners. First, in an inline fashion, where the back-ticks (&#96;code here&#96;) are used to form inline code that has `this` appearence. The second form where code can appear is in multiline code using tripple back-ticks (```). Here are the syntax for each of these :

```md
syntax : ```[language]
 code
``&#96;
inline : `code`
```

###### JavaScript code example
```javascript
  setInterval(()=>{
    let a = document.getElementById("clock");
    // require a new Date  
    let d = new Date(); 
    let minutes = d.getMinutes(); 
    let seconds = d.getSeconds(); 
    let hours = d.getHours(); 

    a.innerHTML = `${hours}, ${minutes}, ${seconds}`;
}, 10);
```

###### JavaScript inline code
`const code = "some string here";`

Here you can see that these two code blocks are different. The one with the triple back-sticks is more visual because it has syntax highlighting to make it more visible and appealing to the eye, but only if a language name is precised. The inline code, with only 2 back-sticks is only for short code blocks or commands like a command in the cmd, for example. 

## Tables
A bit sooner in the guide, I have used a table to demonstrate the different emphasis that could be used with text. Now, we are going to the table itself. Unlike *HTML* that uses the `<table></table>` tag, you have to manually writte your tables in Markdown. Please note that before trying tables, that some Markdown readers will not render tables, so it may be restricted to some but most of the parsers. Here is the syntax to use when writting tables : 

```md 
| name    | cost   | taxes   |
|  -----  | ------ | ------- |
| bicycle | 120$   | 15%     |
| house   | 10000$ | 25.5%   |
| computer| 3000$  | 18%     |

```
result : 

| name    | cost   | taxes   |
|  -----  | ------ | ------- |
| bicycle | 120$   | 15%     |
| house   | 10000$ | 25.5%   |
| computer| 3000$  | 18%     |

###### Note that tables can also be written under the *HTML* syntax

## HTML 
HTML can be used with Markdown to create some effects, but it is limited. First, inline HTML does not work greatly with Markdown. Second, attributes such as classes and ids won't serve much because Markdown's CSS cannot be changed. I also have to mention that objects such as `<canvas></canvas>` do not have a great use in Markdown because they cannot display images or such that require Javascript or other files to intervene with it. Here are some useful tags in html, that we can use here :

1. `<a></a>` - can be used to mark links in the document
2. `<sup><sup>` - can be used to reference a source in the document & exponents 
3. `<table></table>` - if you are not content with the Markdown table syntax


## Media 
Media refers to elements to broadcast information. In this case we are going to talk about how to integrate videos and images onto a Markdown document. Before you use HTML for everything, let me tell you that it does not work exactly going to plan. But here is how you can get a video and an image working in your Markdown document :
```md 
syntax : ![placeholder text](source) - image 
syntax : [![placeholder text](thumbnail image source)](youtube video id) - video
```


###### an image example :
![a field somewhere i don't know](data:image/jpeg;base64,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)
###### A video example :
[![not a rickroll](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

## Anchors
Anchors or links, are elements that go onto another page or somewhere different in the same page. In Markdown there are many ways of writting links. First, you could just write it as plain text, but there is actually other ways of writting links. Here are some different syntaxes that you can use to write links :
```md
1. plain text : https://www.youtube.com/watch?v=dQw4w9WgXcQ;  - Rickroll
2. with a reference : [not a rickroll](https://www.youtube.com/watch?v=dQw4w9WgXcQ)  - Rickroll
3. a file reference : [reference](../readme.md)  - the readme.md at the start 
```
1. plain text : https://www.youtube.com/watch?v=dQw4w9WgXcQ; 
2. with a reference : [not a rickroll](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
3. a file reference : [reference](../readme.md)
