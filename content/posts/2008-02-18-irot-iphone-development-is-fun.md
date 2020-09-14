---
title: iRot - iPhone development is fun
date: 2008-02-18T21:00:00
---

Over the weekend I decided to try my hand at a little iPhone
development. My Objective-C skill is non-existant, and my C skill is
incredibly rusty - but I pressed on. First up was installation of the
toolchain required to compile native applications. This one was tough,
very tough. After much swearing and shouting, I finally managed to get
it to install. The iPhone dev team's official instructions were of help
right up until

```bash
sed 's/^FLAGS_FOR_TARGET=$/FLAGS_FOR_TARGET=${FLAGS_FOR_TARGET-}/g'
```

This is where things seemed to go horribly wrong for me and others.
After scouring google for solutions for what seemed like hours, I
finally happened up on
[this](http://www.kdbdallas.com/index.php/2007/11/16/help-with-building-the-iphone-leopard-toolchain/)
little golden nugget. With the toolchain finally installed I cracked
open my copy of Stephen Kochan's [Programming in
Objective-C](http://www.amazon.com/Programming-Objective-C-Developers-Library-Stephen/dp/0672325861)
along with [iPhone Open Application
Development](http://www.oreilly.com/catalog/9780596519513/?CMP=ILC-Home3&ATT=9780596519513)
- a book by NES.app's developer which I really can't recommend at the
moment.

I decided to write a useless little ROT13 app which you can grab by
adding `http://www.jasonmadigan.com/repo.xml` to your installer.app's
repository list. I'll release the source tomorrow after a quick cleanup.
