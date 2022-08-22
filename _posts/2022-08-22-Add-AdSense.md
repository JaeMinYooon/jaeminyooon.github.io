---
layout: post
title: "깃허브 블로그에 AdSense 추가하기"
date: 2022-08-22T02:25:52-05:00
author: Jaemin
categories: Blog
---

귀찮지만 github blog를 사용하는 사용자를 위해.. (나중에 더 자세하게 포스트 할 예정)

<h2>0. 애드센스 사전작업</h2>
[구글 애드센스](http://www.google.com/adsense/)에서 사이트 신청을 해야한다.

<h2>1. 블로그에 애드센스 넣기</h2>
사이트를 연결하면 광고를 넣을 예시와 같은 코드를 알려준다.
```
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-1647799186209550"
     crossorigin="anonymous">
     </script>
```
해당 코드를 `_layouts/default.html` 속 html태그 안에 넣어주면 된다.

<h2>주의 사항</h2>
구글 애드센스에서 신청을 했다고 다 받아주는 것이 아니다. 
신청하기 전에 어느정도의 블로그를 운영해서 방문자와 게시물을 모으고 하길 바란다.
