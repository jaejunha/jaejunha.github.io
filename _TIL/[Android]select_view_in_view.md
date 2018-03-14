---
layout: post 
tag: Android
title: Select View in View
date: 2018.03.14
---

## Select View in View  
If you want to choose view which was in parent view, use **findViewById()** method   
below code is example
```
list_type.setOnItemClickListener(new AdapterView.OnItemClickListener() {
	@RequiresApi(api = Build.VERSION_CODES.O)
	@Override
	public void onItemClick(AdapterView<?> adapterView, View view, int i, long l) { 		
		((TextView)view.findViewById(R.id.text_item)).setText("Hello");
	}
});
```
To use custom Listview contents, I made a layout which includes TextView   
So, view points Listview contents. <u>If want to choose inner view</u>(In my case, inner view is TextView), then you'd better use **findViewById()** method which can help you access inner view  