# petzku's Aegisub scripts

Automation scripts for Aegisub. These are probably mostly useful for typesetters, if anyone.

## Required modules

### DependencyControl

Scripts I make will use [DependencyControl](https://github.com/TypesettingTools/DependencyControl) for versioning and dependency management.

## Scripts

### Clip Size

Tells you the distances between points in a vector clip on the selected line. The utility of this is debatable, but I find it useful to quickly compare sizes of similar signs or text in different parts of the video.

### Extrapolate Move

Takes a line with a partial-duration move and extends it to the line's full duration. For instance, a line with duration of 3000 ms and a movement of `\move(320,200,520,100,1000,2000)` would end up with `\move(120,300,720,0)`. Useful for doing linear movements when you can't align the start and/or end points with traditional means (maybe because they're offscreen).

### Jump to Next++

Adds a mode to unanimated's [Jump to Next](https://github.com/unanimated/luaegisub/blob/master/ua.JumpToNext.lua) script, allowing you to jump by lines' start and end times. The script should work standalone too, if these are the only features you want out of it.

### Typewriter

Takes a line and "writes" it character by character, making the characters appear one by one (using alphas) either frame-by-frame or evenly spaced over the line's duration. My first script, initially made before I even knew what the hell alpha-timing was and actually deleted characters from the string to make this work. Obviously this has been changed since.

Currently does not play well with `\move` or `\t` tags. There's a good chance another script does what this one does already, except better. Might also eventually implement right-to-left and/or bottom-to-top writing.
