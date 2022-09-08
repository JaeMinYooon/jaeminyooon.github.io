---
layout: post
title: "homebrew install error"
date: 2022-09-06T02:25:52-05:00
author: Jaemin
categories: Blog
---

homebrew를 설치 한 후에도 
```
zsh: command not found: brew
```
와 같은 에러가 계속 나온다면

```
   eval $(/opt/homebrew/bin/brew shellenv)
```
로 해결하면 된다.

맥북 m1칩을 탑재한 새로운 맥에서는 이러한 에러가 나타나는 듯 하다.