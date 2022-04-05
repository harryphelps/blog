---
title: "How to Add Untracked Files Without Committing Them"
date: 2022-04-05T16:15:59+01:00
draft: false
---
Today I learned that you can use `git add -N <file-name>` to stage an untracked file without committing it. This came in handy when I needed to rework a PR with some untracked files in and they kept disappearing when I reset the branch. I added them one by one with the `-N` option, and when they were no longer untracked I was able to rework the PR without fear. 
