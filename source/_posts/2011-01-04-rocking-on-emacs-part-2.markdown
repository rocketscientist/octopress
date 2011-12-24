---
layout: post
title: "Rocking on Emacs, part 2"
date: 2011-01-04 00:18
comments: true
categories: 
---

My Emacs still wasn't as good as I wanted it to be, so I took some time to iron out the little details. For things like a text editor, a minor productivity losses like how needing to resize the window to fit my screen can add up since I'll be using Emacs dozens of times a day.

<!-- more -->

**Minor annoyance #1: window size**

When I pull up Emacs when my laptop is hooked up to my 19" monitor, the window height and width is perfect. But when I unplug and use my laptop screen, the height of the window is larger than the height of the screen and the all-important mini-buffer at the bottom of the window gets cut off. I can always resize it, but it's a pain. Besides, there is something funky about how Ubuntu handles window resizing -- the tolerance so fine, it is actually hard to position the pointer close enough over the edge of the window for it to turn into a "grabber tool". (I'll fix this problem another day.) That aside, *real* programmers don't use the mouse.

Solution: [http://stackoverflow.com/questions/92971/how-do-i-set-the-size-of-emacs-window](http://stackoverflow.com/questions/92971/how-do-i-set-the-size-of-emacs-window)

**Minor annoyance #2: install emacs modes**

When I edited a simple HTML document, I realized I didn't have HTML mode. Turns out installing packages is easy as pie. Type:

    M-x package-list-packages

New buffer with list of available packages will open and you can select those you want to install. Just place the cursor on the package line and press `i`. When you are finished with selection press `x` and packages will be installed. At any time you can press `h` to get quick help for Elpa packaging system. In order to uninstall package you have to press `d` (and `x` after that).

Restart emacs for things to take effect.

**Minor annoyance #2.5: proper way of doing customizations**

Instead of modifying the core code as I suggested earlier, turns out you can put individual customizations in a folder named after your username. My customizations are now located in `~/.emacs.d/samuel` and is tracked by Git in a separate branch. This way, I can rebase whenever a new version of emacs-starter-kit comes out.

I put the window fix in `customizations.el` and the color theme selection in `color-library-theme.el`
