---
layout: post 
tag: Android
title: Implement Drag
date: 2018.03.05
---

## Implement Drag
There are several method to use drag function  
However I'll introduce one method to use **OnTouchListener**  
So, implement OnTouchListener  
```
class YourClass implements OntouchListener{
...
```
Then override **onTouch** method  
```
@Override
public boolean onTouch(View view, MotionEvent motionEvent) {
}
```
To implement drag function, you need **three action** : *ACTION_DOWN, ACTION_MOVE, ACTION_UP*  
action | description
-|-
ACTION_DOWN | When you touch screen, it is called   
ACTION_MOVE | When you move your finger, it is called   
ACTION_UP | When you remove your finger from screen, it is called   
You **can distinguish** three action using **switch** statement  
In addition, you must follow the order : ACTION_DOWN - ACTION_MOVE - ACTION_UP  
```
public boolean onTouch(View view, MotionEvent motionEvent) {
	switch (motionEvent.getAction()) {
		case MotionEvent.ACTION_DOWN:
			//some events;
			return true;
		case MotionEvent.ACTION_MOVE:
			//some events;
			return true;
		case MotionEvent.ACTION_UP:
			//some events;
			return false;
		}
	return false;
}
```
You must return **false in ACTION_UP**, **true in ACTION_DOWN, ACTION_MOVE**  
## Coordinates  
When you want to know coordinate, you must use **motionEvent.getRawX()** or **motionEvent.getRawY()**  
It is good to use **getRawX() rather than getX()** because of accuracy  
