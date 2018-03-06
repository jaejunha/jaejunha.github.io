---
layout: post
tag: Git
title: Change commit date
date: 2018.03.06
---

## Change commit date  
If you want to change commiter date
```
GIT_COMMITTER_DATE="<date>"
example of <date> : Tue Mar 6 16:57:16 2018 +0900
```
  
If you want to change author date
```
git commit --amend --date="<date>"
example of <date> : Tue Mar 6 16:57:16 2018 +0900
```

If you want to change both commiter date and author date
```
GIT_COMMITTER_DATE="<date>" git commit --amend --date="<date>"
example of <date> : Tue Mar 6 16:57:16 2018 +0900
```