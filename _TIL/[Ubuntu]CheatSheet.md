---
layout: post 
tag: Ubuntu
title: CheatSheet
date: 2018.05.03
---

## CheatSheet  

|명령어|설명|
| :--- | :--- |
|`apt-get install <packege>`|패키지를 설치한다|
|`wget <url-address>`|파일을 인터넷으로부터 다운로드 한다|
|`dpkg-reconfigure tzdata`|time zone을 바꾼다|
|`export <environment-variable>=<value>`|환경 변수를 설정한다|
|`unset <environment-variable>`|환경 변수를 삭제한다|
|`halt`|시스템을 즉시 종료시킨다|
|`tar -czvf <file-name>.tar.gz <file-name>`|파일을 tar.gz파일로 압축시킨다|
|`tar -xzvf <file-name>.tar.gz`|tar.gz파일의 압축을 푼다|
|`tar -cvf <file-name>.tar <file-name>`|파일을 tar파일로 압축시킨다|
|`tar -xvf <file-name>.tar`|tar파일의 압축을 푼다|
|`unzip <file-name>`|zip파일의 압축을 푼다|
|`passwd <user-id>`|특정 사용자의 비밀번호를 바꾼다|
|`gedit <file-name>`|파일을 gedit으로 연다|
|`cat <file-name>`|파일의 내용을 콘솔에 출력한다|
|`grep <pattern> <file-name>`|파일에서 특정 패턴을 찾는다|
|`find <directory> -name <file-name>`|특정 경로에서 특정 파일을 찾는다|
|`find <directory> -name <file-name> | xargs grep <pattern>` |특정 경로에서 특정 패턴을 가진 파일을 찾는다|
