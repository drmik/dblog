---
title: "Deleting Globally Installed npm Packages"
date: 2019-09-05T16:52:34+01:00
---

The npm package manager can install packages in project directories or globally (i.e. in your `/usr/local/bin/` directory).

Fortunately, deleting a project removes all associated npm packages — since the packages are installed within the project directory.

However, for globally installed packages, you’d first have to list them using:

```
npm list -g --depth 0
```

This command to print to screen all top-level packages install using the npm install -g ... command. For example:

```
/usr/local/lib
├── fkill-cli@4.1.0
├── ngrok@3.0.0
├── npm@6.11.2
├── spaceship-prompt@3.11.1
└── tldr@3.1.1
```

To delete package from the list printed to screen, simply run:

```
sudo npm uninstall -g package1 
```

Note that, you could include more than one package after the -g option.
