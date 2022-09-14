---
layout: post
title: "github publickey permission denied"
date: 2022-09-13T02:25:52-05:00
author: Jaemin
categories: Github
---

<h2>0. Permission denied (publickey).</h2>
아마 새로운 pc로 ssh git clone을 하게되면 git@github.com: Permission denied (publickey). 라는 에러가 나올 것이다.
git@github.com에 연결된 ssh key가 설정되어 있지 않기 때문인데, 한번만 하면 쭉 사용 가능하기에 pc가 바뀔때 쯤이면 까먹는 경우가 많다.

<h2>1. ssh key 만들기</h2>
```
1. ssh-keygen -t rsa -C "사용할 github 계정 이메일" 입력
2. 어느 위치에 넣을 지 (엔터를 누르면 디폴트 위치에 생성(~/.ssh/id_rsa)
3. 비밀번호 입력 (엔터를 누르면 비밀번호가 없이 생성)
    * 비밀번호는 나중에 ssh로 git clone할 때 마다 물어보니 외워야 함
```

<h2>2. Github setting</h2>
```
1. github 로그인
2. 우측 상단 자기 프로필 클릭 (알림종, +, 프로필)
3. Settings 클릭
4. 새로운 화면에서 New SSH Key 클릭
5. 1-2에 저장한 위치에서 id_rsa.pub파일을 열고 key값을 복사
6. SSH Key 값 입력하는 곳에 붙여주기
```

<h2>3. Test</h2>
```
$ ssh -T git@github.com
```
ssh key가 잘 들어갔다면 위 코드를 입력 시
Hi (사용자 이름) You've successfully authenticated. but GitHub does not provide shell access.
라고 나올 것이다. but이라는 문구 때문에 안된 것 같지만 문제없이 성공한 것이니 git clone을 시작하면 된다.
