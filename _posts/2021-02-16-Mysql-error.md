---
layout: post
title:  "Mysql에서 foreign key 무시하고 데이터 삭제하는 방법"
date:   2021-02-16T14:25:52-05:00
author: Jaemin
categories: Mysql
---

<h2>Mysql에서 foreign key 무시하고 데이터 삭제하는 방법</h2>

SET foreign_key_checks = 0;

truncate or delete

SET foreign_key_checks = 1;


