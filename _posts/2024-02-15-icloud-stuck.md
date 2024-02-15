---
title: How to Solve 'iCloud Stuck on Uploading'
date: 2024-02-15 16:00:00 +/-TTTT
categories: [Tech]
tags: [icloud]     # TAG names should always be lowercase
---

I just noticed that the iCloud Drive kept 'uploading' something and stuck there forever. 

I do not know the reason but it is really annoying.

How I solve it:

## Kill 'bird' process

I guess this process relates to the uploading action of iCloud drive.

Anyway, you can easily kill them by typing:

```bash
killall bird
```

I know there are other ways to kill the specific process but just try this. 

## Remove 'CloudDocs' folder

Sometimes after you kill the bird processes the uploading action will be reset.

But it does not apply to my case.

What I did then was to remove the CloudDocs folder, which will force the iCloud Drive to redownload everything.

Simply rm -rf may not work , my suggestion is to rename it or move it to another place, then kill the bird process.

It may cost you more time but usually the issue will be resolved.

