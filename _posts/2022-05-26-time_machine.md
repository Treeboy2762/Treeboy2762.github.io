---
layout: post
title: External SSD recognized as time machine
subtitle: SSD로 사용하고 싶은데 자꾸 time machine으로 인식된다.
description: >-
  After *accidentally* clicking on time machine, Mac keeps recognizing the SSD as a backup drive
image: >-
  /assets/img/posts/post4_success.png
optimized_image: >-
  /assets/img/posts/post4_success.png
category: blog
tags:
  - blog
author: daesungkim
paginate: true
---
Date Published: {{ site.time | date: '%B %d, %Y %r' }}

Weird phenomenon.

For some unfathomable reasons, my dear Jihoo used her Samsung T7 SSD as a time machine backup drive. The problem is, as the drive is recognized as a AFPS backup drive, it is "read-only." Surprisingly, other Mac devices normally recognize the problematic SSD as a normal external drive. I tried removing disk from Time Machine (in the preferences) but yielded no fruits.

## Solution

First, I deleted associated backup files.

- Grant Full Disk Access to terminal (can be done in the preferences)
- cd into the external drive
- Use ls to locate backups. It looks like 2021-05-22-195414.inprogress.
- Use rm -rf to delete the backup folder
- I also deleted backup_manifest.plist file just in case

This may have been a stepping stone to victory, but I needed additional breakthrough.

I got the inspiration from [This stack](https://apple.stackexchange.com/questions/420422/time-machine-stopped-recognising-backups-on-the-nas-storage-and-does-not-make-ne).

Apparently, Mac required manual "changeVolumeRole" to no longer recognize the drive as a time machine backup drive.

After typing `diskutil apfs changeVolumeRole /dev/disk3s2 t` to the terminal, the SSD became normal as desired.