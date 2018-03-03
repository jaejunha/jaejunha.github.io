---
layout: post 
tag: Android
title: View Capture
date: 2018.02.21
---

## View Capture
To capture contents of view, you use following functions
```
view.setDrawingCacheEnabled(true);
view.setDrawingCacheBackgroundColor(0xfffafafa);
view.getDrawingCache().compress(Bitmap.CompressFormat.JPEG, 100, outputStream);
setDrawingCacheEnabled(false);
```
