---
layout: post
title: "Ruby eccentricities"
date: 2010-12-27 18:29
comments: true
categories: 
---

Coming from a C, C++, PHP, and Java background, Ruby is a little different. Here's a list of things that are a little... unorthodox to me:

<!-- more -->

The `nil` object evaluates to false in a boolean context, apart from `false` itself. For example, any `if` statement that tests a `nil` is false. All other Ruby objects evaluates to `true`, even zero.

Single-quoted strings: Ruby doesn't interpolate them and they are literal (ie. their output is escaped). But other than that, they are the same as double-quoted strings.

    '\n'       # A literal 'backslash n' combination "\n"

Backwards if statements are allowed.

    puts "Both strings are empty" if x.empty? && y.empty?
    puts "The string '#{string}' is nonempty." unless string.empty?

Ruby functions have an implicit return, meaning they return the last statement evaluated. An explicit return can be declared using the `return` keyword, just like in C++.
