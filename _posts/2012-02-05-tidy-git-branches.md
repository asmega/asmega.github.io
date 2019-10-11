---
layout: post
title:  "Tidy git branches"
date:   2012-02-05
---

Branching in git is an ease to work with and literally takes seconds. You can be working on your own feature, switch to a colleague's feature then switch to production code to check a bug all within a few keystrokes and in no time at all.

Branching is easy and a convenience. However this often leads to many branches and over time that leads branch hell. We want to be able to clean up all those merged in branches that we were too lazy to delete 3 months ago. Here's the code to do the purge.

<script src="https://gist.github.com/asmega/1620379.js"></script>

If you're working with github or you're storing your code in a 'central' repository you'll likely be experiencing the same thing on the remote server as well. Here's the modified version to purge remote branches.

<script src="https://gist.github.com/asmega/1620431.js"></script>

With these little scripts you can keep periodically prune your branches every so often and not need to this every time and also prevent your repository from over growing.
