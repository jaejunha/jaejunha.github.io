---
layout: post
tag: Git
title: Pull Request
date: 2018.06.04
---

## Pull Request  
1. **fork repository** which you want to contribute  
2. download repository using **git clone https://github.com/\<your name\>/\<repository\>**  
3. enter the repository which you fork: **cd \<repository\>**  
4. add origin address using **git remote add \<alias\> https://github.com/\<owner's name\>/\<repository\>**  
5. fetch updated commit using **get fetch \<alias\>**  
6. change current branch to master using **git checkout master**  
7. merge what you do with original repository commits using **git merge \<alias\>/master**  
8. do some works(eg. write codes)  
9. **git add .**  
10. **git commit -m "\<message\>"**  
11. **git push origin master**  
12. enter your repostory through internet
13. click button:**New pull request**  