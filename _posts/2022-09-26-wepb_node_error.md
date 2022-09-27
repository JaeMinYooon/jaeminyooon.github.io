---
layout: post
title: "TypeError: Failed to parse URL from ~~/webp_node_dec.wasm"
date: 2022-09-26T02:25:52-05:00
author: Jaemin
categories: node error
---

<h2>0. TypeError: Failed to parse URL from  ~~/webp_node_dec.wasm</h2>
webp를 사용할 때 이러한 에러를 발견했다. 해결하려구 여러 곳을 찾아봤는데 이 해결방법이 도움이 되었다. (다른 이미지파일 에러도 비슷하게 해결하는 듯 하다.)

<h2>1. 해결 방법</h2>
[해결 방법](https://github.com/GoogleChromeLabs/squoosh/issues/1260)
여기서 해결 방법을 찾았다. node version을 16으로 낮추면 된다고 한다.

<h2>2. node downgrade</h2>
MAC 기준이고 저처럼 다운그레이드를 또 검색하실 수 있어서 적어두겠습니다.
```
1. node -v // 버전 확인
2. brew search node
3. brew unlink node
4. brew install node@16
5. brew link node@16
6. node -v // 버전 확인
```

<h2>3. 2-5에서 error</h2>
2-5에서 잘 실행이 됐다면 다행이지만 필자는 이런 에러가 나왔다.
```
Error: Could not symlink bin/npm
```
해결 방법
```
1. brew link --overwrite node@16
2. brew link node@16
3. brew unlink node@16
4. brew reinstall node@16
5. brew link node@16
6. node -v // 버전 확인
```
