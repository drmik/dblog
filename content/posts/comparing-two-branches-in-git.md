---
title: "Comparing two Git branches"
date: 2018-09-24T07:24:21+01:00
---

JTo see the differences between two branches in a Git reposiory, use:

```sh
$ git diff branch_1 branch_2
```

If you already have a `difftool` setup (something like Kaleidoscope), you can view the DIFFs using:

```sh
$ git difftool branch_1 branch_2
```

Both commands will produce the diff between the tips of the two branches. The same syntax works for comparing a branch with a tag or a tag with another tag. Note that you can also add a file or folder name after the above two commands.

Source: <https:></https:>