---
layout: post
title: 블로그 테마 이사
subtitle: 더 깔끔한 블로그를 만들어 보자
description: >-
  딱히 설명할 건 없다..
category: blog
tags:
  - blog
author: daesungkim
paginate: true
katex: true
---

![](https://velog.velcdn.com/images/treeboy2762/post/278c2464-b815-423c-a1e2-a895db0661f8/image.png)

맘에 들긴 하지만.. 조금 간단한 디자인을 위해 새 테마를 적용하기로 했다.

https://jekyllthemes.io/free 에서 mundane 이란 테마를 찾아 적용을 해보려고 한다. 

mundana github 에서 테마 폴더를 다운받은 뒤, posts를 모두 옮긴다.

git bash 를 켠 뒤 bundle 을 이용해 설치를 하려 하는데...

![](https://velog.velcdn.com/images/treeboy2762/post/43a31746-fe04-4f30-8d0b-b38cbe205f88/image.png)

어라 안되네? [이 포스트](http://corecode.pe.kr/2020/08/21/ruby_jekyll_install/) 를 참조, bundle update 로 문제를 해결했다.

![](https://velog.velcdn.com/images/treeboy2762/post/e1ab04cc-69f8-4425-b8bc-f1554f8ac27f/image.png)

bundle exec jekyll serve .

--watch?

를 사용해 시뮬레이션을 돌려보자. 만족.

## 디테일 수정

잡일을 할 차례다.

1. 프로필 수정

_config.yml 파일에서 프로필을 적절하게 수정해준다.
_pages/author-daesungkim.html를 만들어준다.
_config.yml 에서 baseurl 을 '' 로 비워준다.


2. katex 적용

적용한지 얼마나 되었다고 다시 해야한다..

https://katex.org/docs/autorender.html 를 따라서 default.html 에 스크립트를 추가해준다.

또한 _config.yml 에서
kramdown:
  math_engine: katex
을 추가해준다.

음.. github pages 는 바로 되는지 모르겠는데 컴퓨터에서 되는지 확인하고 싶기 때문에 [이 포스트](https://www.xuningyang.com/blog/2021-01-11-katex-with-jekyll/#:~:text=How%20to%20LaTeX%20in%20Jekyll%20using%20KaTeX%201,off%20%28optional%29%20...%204%20Step%204%3A%20To%20use) 를 참조해 컴퓨터에도 katex 를 설치해 주도록 한다.

3. 이미지 옮기기

이상하게 포스트 안에 있는 이미지는 / 가 필요하고 그냥 이미지는 / 없이 사용한다.. 그럴거면 그냥 전부 / 있게 하면 안되나..

대략 6시에 시작해서 2시간 반 걸린 것 같다.
