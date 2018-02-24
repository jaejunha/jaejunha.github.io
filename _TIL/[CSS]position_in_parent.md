---
layout: post
tag: CSS
title: Position in parent element
date: 2018.02.24
---

## Situation   
want to place an element <u>at specific location in parent element</u>  
## Solution  
position of parent element sets **relative**   
position of child element sets **absolute**   
## Example  
HTML
```
<div class="parent">
	<div class="child"></div>
</div>
```
CSS
```
.parent{
    position: relative;
    overflow: hidden; //to prevent child element from overflowing parent element 
}
.child{
    position: absolute;
    left: 10px;
    top: 10px;
}
```