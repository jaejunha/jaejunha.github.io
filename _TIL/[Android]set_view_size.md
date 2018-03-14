---
layout: post 
tag: Android
title: Set view size
date: 2018.03.14
---

## Set view size  
If you want to set size of view programmatically, use LayoutParams  
```
ViewGroup.LayoutParams params = view.getLayoutParams();
params.width = 100;
view.setLayoutParams(params);
```