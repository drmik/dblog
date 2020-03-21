---
title: "Keyboard Shortcut for 'Run All Cells' in Jupyter Lab"
date: 2019-10-23T12:50:40+01:00
---

Mastering keyboard shortcuts would likely make you more productive. This is the reason I use [Vim bindings](./vim-bindings-for-jupyter-lab-cells-installing-the-extension) in JupyterLab.

Oftentimes, when running experiments, you'll find yourself restarting the kernel and running all Jupyter cells. Fortunately, JupyterLab the ships with a keyboard shortcut (i.e. `0, 0`) to *Restart Kernel* amongst others.

To define your own keyboard shortcut for running all cell, you can use the approach recommended by [Ran Feldesh](https://stackoverflow.com/users/10006823/ran-feldesh) [on StackOverflow](https://stackoverflow.com/a/57712509).

Basically, all you have to do is to open the Keyboard Shortcut section in your Advanced Settings Editor

> In the top menu, go to: `Settings` » `Advanced Settings Editor` » `Keyboard Shortcuts`

Then, paste this code in the `User Preferences` window:

```json
{
    "shortcuts": [
        {
            "command": "runmenu:run-all",
            "keys": [
                "R",
                "R"
            ],
            "selector": "[data-jp-kernel-user]:focus"
        }
    ]
}
```

Finally, save your changes on the top right of the user-preferences window.

I tend to repeat this process for every new machine I work on, hence I've written it here as a reminder to my future self. Thanks for the tip, [Ran Feldesh](https://stackoverflow.com/users/10006823/ran-feldesh) 🔥.