---
layout: post
title: 첫 포스트 >_<
subtitle: '사실 별 의미는 없다.'
description: >-
  Celebration of the website launch.
image: >-
  /assets/img/posts/post1_1.jpg
optimized_image: >-
  /assets/img/posts/post1_1.jpg
category: blog
tags:
  - blog
author: daesungkim
paginate: true
---

## 잘 되나?

Time Zone 때문에 꽤나 고생했다.

https://present4n6.tistory.com/7?category=904222 를 따라 Gemfile에 'tzinfo'를 지정해 주고,

root의 _config.yml이 아닌 src/yml/_config.yml 파일에서

timezone: Asia/Seoul 로 세팅을 해 주어야 했다...... 하고 끝난 줄 알았는데 아직도 해결이 안되어서 그냥 date 정보를 지운 채로 포스트를 올린다.

(For my reference)

Local에서 preview 하고 싶으면

```js
  cd Documents/Treeboy2762.github.io
  bundle exec jekyll serve
```