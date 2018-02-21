---
layout: post 
tag: Android
title: File Save & View Capture
date: 2018.02.21
---

# Android
## File Save
To save file, must give permission at AndroidManifest.xml
```
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```
Second, open file which you want to save
```
File file = new File(Environment.getExternalStorageDirectory(), "Test.jpg");
```
Third, make file output stream to write you want to write, and save string
```
FileOutputStream outputStream = openFileOutput(file, Context.MODE_PRIVATE);
outputStream.write(string.getBytes());
outputStream.close();
```
## View Capture
To capture contents of view, you use following functions
```
view.setDrawingCacheEnabled(true);
view.setDrawingCacheBackgroundColor(0xfffafafa);
view.getDrawingCache().compress(Bitmap.CompressFormat.JPEG, 100, outputStream);
setDrawingCacheEnabled(false);
```
