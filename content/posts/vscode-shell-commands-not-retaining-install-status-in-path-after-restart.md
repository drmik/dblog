---
title: "VSCode Shell Commands not retaining install status in $PATH after restart"
date: 2019-02-28T16:52:34+01:00
author: Khalil
---

After you download VSCode and [add it to your PATH](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line), you may stumble upon a problem where you cannot launch VSCode from the command line or Terminal --- it's as if something modifies your system PATH and takes out the VSCode entry.

This problem is notoriously annoying. But fret not, there's a [simple solution](https://github.com/Microsoft/vscode/issues/42051#issuecomment-441899647) (for MacOS) users. [Matan Gover](https://github.com/matangover) responded to an [GitHub issue](https://github.com/Microsoft/vscode/issues/42051) related to the problem as follows:

> I was having the same problem, but unlike @benday, I was running VS Code from /Applications (not from ~/Downloads). Turns out I still had the `quarantine` attribute set on VS Code -- probably because I had moved it from ~/Downloads to /Applications using mv instead of Finder. Only moving it [using Finder](http://www.openradar.me/radar?id=5022734169931776) removes the quarantine attribute.
> 
> To fix the issue, I followed the instructions in [#48124 (comment)](https://github.com/Microsoft/vscode/issues/48124#issuecomment-383614238) and ran:
> 
> ```shell
> xattr -dr com.apple.quarantine /Applications/Visual\ Studio\ Code.app
> ```
> 
> IMO since this seems to cause confusion, VS Code should show a warning if "Shell Command: Install 'code' command in PATH" is invoked when running from a read-only file system, as in [Squirrel/Squirrel.Mac#186](https://github.com/Squirrel/Squirrel.Mac/pull/186). Even better would be to offer the user to fix it for them.

I have tested the proposed solution and it works! If you're also having a similar problem with [MacDown's](https://macdown.uranusjr.com/) `macdown` command or [PyCharm's](https://www.jetbrains.com/pycharm/) `charm` command, you now know what to do.