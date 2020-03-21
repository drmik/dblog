---
title: "Vim bindings for Jupyter Lab cells: Installing the Extension"
date: 2019-02-15T07:54:45+01:00
---

![](https://www.vim.org/images/vim_dishwash_bar.jpg)
I've recently discovered the joy of Vim. And indeed, it does increase my coding speed (if that's even a thing 🤔). Thanks to the [`jupyterlab-vim`](https://github.com/jwkvam/jupyterlab-vim) project, you can also get _":neckbeard: Vim notebook cell bindings for JupyterLab"_

To install this JupyterLab extension, activate the appropriate conda environment, then check if [Node.js](https://nodejs.org/en/) is installed

```bash
conda list | grep node
```

If you get an empty output, then it means that node isn't installed. But if your output is something like the one below, you can skip installing node --- because you already have it.

```
nodejs                    10.13.0              he6710b0_0    anaconda
```

To install Node.js using conda, use:

```bash
conda install -c anaconda nodejs --yes
```

Now you're ready to install JupyterLab extensions. Run the following command to install JupyterLab Vim

```bash
jupyter labextension install jupyterlab_vim
```