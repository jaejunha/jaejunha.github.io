---
layout: post
tag: CSS
title: Position in parent element
date: 2018.02.27
---

## Situation   
want to place an element <u>at specific location in parent element</u>  
## Solution  
set **position** of parent element to **relative**   
set **position** of child element to **absolute**   
set **left & top** of child element to **50%**  
set **transform** of child element to **translate(-50%, -50%)**  

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
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
}
```