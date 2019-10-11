---
layout: post
title:  "Install .vpk files on mac"
date:   2013-04-14
---

.vpk files are packaged up add-on files for steam games such as Left 4 Dead 2. To install these files on windows double clicking on the file will do the job. On a Mac that doesn’t work and you’ll have to manually copy the file across.

```
cp /path/to/file.vpk /Users/USERNAME/Library/Application\ Support/Steam/SteamApps/common/left\ 4\ dead\ 2/left4dead2/addons/
```

Or if you are install for another game should be something similar to the above.

```
cp /path/to/file.vpk /Users/USERNAME/Library/Application\ Support/Steam/SteamApps/common/GAME/GAME/addons/
```

Make sure to replace USERNAME for your login username.
