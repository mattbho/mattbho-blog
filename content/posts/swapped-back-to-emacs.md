+++
title = "Swapped Back to Emacs"
author = ["Matt Ho"]
date = 2026-07-17
draft = false
+++

I swapped back to Emacs lol.

If you read my last post, I'd gone terminal-first - tmux, then herdr, Claude Code living in a multiplexer with Emacs as a companion rather than the host.
I'm undoing that....


## herdr was awesome, and also not enough {#herdr-was-awesome-and-also-not-enough}

herdr genuinely was pretty sick.
Running a multiplexer felt awesome again, and there's something really sweet about interfacing with Claude through a native terminal.

But that was simply it.
When I actually broke down what herdr was giving me, it was notifications - agent-aware ones, sure, nicely done ones, but notifications.
And it turns out I don't need notifications that much at all.

Sure it gave me persistent sessions and agent states but I never needed to use it because I never close my sessions!

I'd already built the same thing with a osascript hook and it worked with Emacs (to my surprise).

Meanwhile I was trading away a lot of my superpowers to get there.


## What I was actually giving up {#what-i-was-actually-giving-up}


### Dired {#dired}

I use dired all the time - dired is a full file system manager for me.
I navigate folders, create folders and files, rename them, change permissions.
It's amazing because its literally the output of `ls`, except interactive.


### gptel {#gptel}

I like gptel.
When I'm reading something and need a quick explain, or just want to talk to Claude like a web chat that isn't scoped to code, gptel is right there in the same environment.


### Magit/ediff magic!! {#magit-ediff-magic}

Noone can convince me that there is a better git interface than magit. There are so many copycats out there. Even Neovim has neogit. All falls flat to the cohesiveness and the magic of magit. Then that paired with ediff gives me a cohesive git hunking and diffing tool.

I even tried flirting with going back to Neovim during all this. I rebuilt my whole config to emulate all of my emacs keybinds. Granted, I will say the editing experience is so smooth and is in a league all of its own. But there lies the problem, I am NOT editing code anymore. I am reading code, and navigating code, and that makes emacs unmatched.


## Back to Emacs now with improvements. {#back-to-emacs-now-with-improvements-dot}

`claude-code-ide.el` actually fulfills my needs way more than I had thought previously.
I can toggle the buffer on and off, manage buffers/sessions the same way on herdr, and the ediff integration is genuinely amazing. - I can review Claude's proposed changes via ediff and edit them live, in real time, as it's proposing them. This package also supports ghostel as its renderer so I would even argue that the interface is even BETTER for my needs than a terminal first workflow.

For long-running sessions I'm using `ghostel` - a terminal emulator for Emacs powered by libghostty-vt, the engine behind the Ghostty terminal.
Featureful, fast, robust, true color, the Kitty keyboard and graphics protocols, hyperlinks, desktop notifications and much more.

This package was literally a gamechanger. It turns emacs into a fully fledged terminal emulator. Literally, all my problems solve.

I'd repent fully for the sins I have commited and announce my return to the Church of Emacs!!!
