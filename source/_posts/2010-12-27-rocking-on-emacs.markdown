---
layout: post
title: "Rocking on Emacs"
date: 2010-12-27 16:18
comments: true
categories: 
---

Emacs has been my editor of choice for the past several years, mostly because
a lot of people in the lab used it. Naturally, Emacs is will be my default editor 
for the [Unstash project](http://unstash.com). Quite a large number of people who 
use Rails also use Emacs, so I'm in good company. Here is a list of some things 
I did to get Emacs and Rails to play along.

<!-- more -->

1.  Installed the [Emacs Starter Kit](https://github.com/technomancy/emacs-starter-kit)

    This is a complete package, and includes:
    *  syntax highlighting for Ruby, HTML, CSS, YML... there are probably more
    *  various color themes
    *  code-completion and auto indenting
    *  a handy filename browser in the mini-buffer

    It was a simple install. Just unzip to `~/.emacs.d/`. The only trick is that I had to remove `~/.emacs` since it came with my Ubuntu 10.10 install.

2.  Chose my color scheme.

    I like dark themes. So I selected the "blackboard" theme. I added the following to the bottom of `~/.emacs.d/init.el`

        ;; set default color theme
        (color-theme-blackboard)

    You can manually select a color theme via `M-x color-theme-` and hitting Tab to bring up a list of completions. The ones that are available out-of-the-box are zenburns, twilight, and blackboard.

3.  Watched the free preview of the "[Meet Emacs](http://peepcode.com/products/meet-emacs)" peepcode screencast.

A good solid intro to powerful Emacs features. I learned some new keybindings for Git -- I wished I knew these in grad school! I'm thinking of buying the whole screencast. I'm sure I can google around to learn on my own, but having someone collect everything together in one place will save me lots of time. Plus, screencasts are cool.
