---
layout: post 
tag: Android
title: Get view size
date: 2018.03.14
---

## Get view size  
If you want to know size of view, you must use view.getWidth() or view.getHeight(). However, we can get size of view right after activity is started. In this situation, using **post thread** is best choice to get size
```
ImageView image = (ImageView) findViewById(R.id.image);

image.post(new Runnable(){
	@Override
	public void run() {
		width = image.getWidth();
		height = image.getHeight();
	}
});
```