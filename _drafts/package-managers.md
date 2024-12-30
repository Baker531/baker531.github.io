---
layout: post
title: MacPorts + Aseprite = Awesome
author: Baker
description: How MacPorts is better than Homebrew
topic: Mac package managers
---
Sadly, the most common Mac package manager is Homebrew. Homebrew is not the best package manager. Here's why.
1. Homebrew only works on new MacOS versions.  
    They have absolutely no support for older versions. It says: 

        Warning: You are using macOS [whatever your version is].
        We (and Apple) do not provide support for this old version.
        It is expected behaviour that some formulae will fail to build in this old version.
        It is expected behaviour that Homebrew will be buggy and slow.
        Do not create any issues about this on Homebrew's GitHub repositories.
        Do not create any issues even if you think this message is unrelated.
        Any opened issues will be immediately closed without response.
        Do not ask for help from MacHomebrew on Twitter.
        You may ask for help in Homebrew's discussions but are unlikely to receive a response.
        Try to figure out the problem yourself and submit a fix as a pull request.
        We will review it but may or may not accept it.
    
    So rude. Meanwhile, MacPorts supports many old versions (back to Montery at the time of writing) fully, and many more partially.
2. Homebrew uses its weird beer terminology.  
    Like `cask`, `caskroom`, `formulae`, `keg`, `cellar`, `bottle`, `tap` and others. But MacPorts uses more traditional language that would be familiar to someone who has already used a different package manager. This is great for beer nerds, but less good for the rest of us.
3. Homebrew relies on system libraries. This means that if, for example, a program you installed used version 3.8 of Python, but your OS had version 3.7, and that program relied on a feature exclusive to version 3.8, it would break. Though, to be fair, this cuts both ways. If you have 20 packages using Python, then you have 20 versions of Python. If Python is 100mb, then that's 2gb. That's a lot for Python.
4. Homebrew messes with the OS.  
    Homebrew takes over usr/local. It sets you as the owner, which is messy. If there's anything already in there, that's not good. But MacPorts uses opt/local, which is entirely for MacPorts. Nothing else uses it. But that does have its issues. It means you need root access, which not everybody has. But it's not a deal breaker, as you can install and use it via a special method (see [MacPorts official instructions](https://www.macports.org/install.php#source) and [GitHub Gist](https://gist.github.com/daggerok/d6c7ed8b9efa03b30ffd0e9f44cdd121)) that doesn't require root access. It installs it in a different location.

## Cons of MacPorts
SUDO

## Wrapping up
GO MACPORTS!!!