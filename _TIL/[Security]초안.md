---
layout: post 
tag: Security
title: 초안
date: 2018.03.25
---

작성할 것들
- SQL injection  
- Race Condition Attack  
- Buffer Overflow   

##리눅스 권한?  
리눅스는 12비트로 파일을 관리한다   
특수 3비트 - 유저 3비트 - 그룹 3비트 - 기타 3비트  

###Set UID  
특정 프로그램은 실행하려면 특정 capacity가 필요  
하지만 루트 권한으로 사용할 시 capacity가 없어도 모두 실행 가능  
capacity가 설정되지 않은 특정 프로그램을 실행 해야될 때, **유저의 권한을 임시로 올려주는 것이 Set UID**  
기한은 **프로그램 실행이 마칠 때**까지  
대표적인 프로그램으로는 ping과 passwd가 있다.  