---
layout: post
title: Linux on VirtualBox
subtitle: Linux on VirtualBox
description: >-
  VirtualBox에서 Linux를 설치해 vim과 grep을 사용해 보자.
image: >-
  /assets/img/posts/post2_2.png
optimized_image: >-
  /assets/img/posts/post2_1.png
category: blog
tags:
  - blog
author: daesungkim
paginate: true
---
Date Published: {{ site.time | date: '%B %d, %Y %r' }}

근데 이거 포스트 쓰는게 너무 귀찮다... 다른 사람들도 vscode에서 포스트를 쓰는 이 불편함을 감수하고 쓰는걸까? Jekyll로 블로그 만드는건 어렵지 않은 거 같은데..

하여튼, 오늘은 [가상머신에 linux를 설치](https://mainia.tistory.com/2379)해서 vim을 사용해 보았다.

두가지 문제점이 생겼었는데..

1. 설치 도중 계속하기 버튼이 잘림

  [Alt F7](/https://askubuntu.com/questions/755196/i-cant-see-the-next-button-ubuntu-installation-on-vmware) 을 사용해 버튼을 찾아준다.

2. cd 를 하려는데 한글을 못침

  ![절망](/assets/img/posts/post2_cantkorean.png "절망")

  해결책은 [이 지침을 따라라](https://hunsdev.tistory.com/3).

  <del>이런거 좀 설치할때 해결해주면 안되나?<del>

추가적으로, 

![한글 모드로 시작](/assets/img/posts/post2_hangul.png "한글 모드로 시작")

오른 쪽 위에 언어 -> 설정 -> 한글 모드로 시작 체크해 놓으면 일일이 한글 설정 체크할 필요가 없어 편리하다.

vim과 grep은 쓸일이 있을지는 솔직히 잘 모르겠다만.. 신박하긴 했다.