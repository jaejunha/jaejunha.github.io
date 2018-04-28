---
layout: post 
tag: Ubuntu
title: CheatSheet
date: 2018.04.29
---

## CheatSheet  
```
apt-get install <packege>				//install package
wget <file-address>						//download files

dpkg-reconfigure tzdata					//chage time zone

export <environment-variable>=<value>	//make or modify environment variable
unset <environment-variable>			//delete environment variable

halt									//shut down system immediately

tar -czvf <file-name>.tar.gz			//zip file
tar -xzvf <file-name>.tar.gz			//unzip file
tar -cvf <file-name>.tar				//zip file
tar -xvf <file-name>.tar				//unzip file

passwd <user-id>						//change user's password

gedit <file-name>						//open file with gedit

cat <file-name>							//printf contents of file at console

grep <pattern> <file-name>				//find pattern in a specific file

find <directory> -name "*.txt"			//find text files in specific directory
find <directory> -name "*.txt" | xargs grep hello	//find text files which contain word: "hello" in specific directory

```