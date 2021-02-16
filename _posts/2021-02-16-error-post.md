---
title: Error
date: 2021-02-16 08:26:28 -0400
categories: error update
---
Mac에서 port의 pid 찾아서 삭제 하려고 하는데 안될 때
-> kill -9 `lsof -i TCP:PORT | awk '/LISTEN/{print $2}'`

Mysql에서 foreign key 때문에 삭제가 안될 때
SET foreign_key_checks = 0;
truncate or delete
SET foreign_key_checks = 1;


[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
