---
layout: post
title: "rm: /PATH_TO_FILE not removed: Disc quota exceeded"
date: 2010-05-29
---

This occurred whilst using Solaris on Joyent. Somewhat annoying when one can't remove a file when `Disc quota exceeded`!

What one can do is override the file contents with nothingness.

```
cat /dev/null >/PATH_TO_FILE
```

Source: [Joyent forums](http://forum.joyent.com/viewtopic.php?id=26181)
