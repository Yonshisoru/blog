---
title: "Basic Md Syntax"
date: 2022-02-10T15:38:01+07:00
draft: false
tags: ['markdown']
categories: ['syntax']
cascade:
  banner: '/blog/duck.jpg'
---
# Syntax
___
## Header
># Header level 1
>## Header level 2
>### Header level 3
>#### Header level 4
>##### Header level 5
>###### Header level 6
```
# Header level 1 | ===
## Header level 2 | ---
### Header level 3
#### Header level 4
##### Header level 5
###### Header level 6

```

## Emphasis
>**Bold**  
>*Italic*  
>***Bold&Italic***
```
    **Bold** | __Bold__
    *Italic* | _Italic_
    ***Bold+Italic*** | ___Bold+Italic___
```
## Blockquotes
>bigest
>>bigger
>>>big
```html
> phares
>> phares
>> phares
```
## List
- 1
- 2
- 3
    - 3.1
    - 3.2
- 4

1. 
2. 
3.  
    3.1  
    3.2  
4.  
- 1968\. A great year!
- I think 1969 was second best.
```
    -*+ 1 | 1. 
    -*+ 2 | 2. 
    -*+ 3 | 3. 
        - 3.1 | 3.1
        - 3.2 | 3.2
    -*+ 4 | 4.
    - 1968\. A great year!
    - I think 1969 was second best.
```
## Image
_normal_
![Duck](/blog/duck.jpg)  
_clickable_
[![Duck](/blog/duck.jpg)](/blog/duck.jpg)
```
![Duck](/<dir>)
[![Duck](/<dir>)][dir] (clickable)
```
## Code
`helloworld`
```
`helloworld`
```
## Escaping Backticks(`)

``Use `code` in your Markdown file.``

```
``Use `code` in your Markdown file.``
```
Horizontal Rules
---
***
---
___
```
***
---
___
```
## Links
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").  
``My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").``
## URLs and Email Address  
<https://www.markdownguide.org>  
<fake@example.com>
```
<https://www.markdownguide.org>
<fake@example.com>
```

## Formatting Links

I love supporting the **[EFF](https://eff.org)**.  
This is the *[Markdown Guide](https://www.markdownguide.org)*.  
See the section on [`code`](#code).  
```
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).
```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole][1], and that means comfort.  

## Escaping Characters
`` \ * _ {} [] <> () # + - . ! | ` ``  

\* Without the backslash, this would be a bullet in an unordered list.  
``` \* Without the backslash, this would be a bullet in an unordered list.  ```