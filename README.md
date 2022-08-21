# CUBS - Caprice Unified Base System 

For the past couple of months, we needed a CLI installer for the server operating system we were working on. We had the experience of using [Calamares](http://calamares.io) but it needs _X Window System_ and at least a window manager or desktop environment. 

We just wanted something as simple as possible, without any outside dependencies, and we came up with this project. This project is inspired by older system installers used on distributions such as Arch Linux or Slackware, but we wrote the whole thing with a modern approach. 

The goal of this project is to provide a _generic installer_ for the whole GNU/Linux ecosystem. If you take a look at the code, you'll understand it acts as agnostic as possible. By the way, there are some issues to be solved: 

- It copies the `filesystem.squashfs` on the disc. So, It means it only installs the version you have on the disk and for future upgrades, you need to upgrade the _installed_ system manually. 
- It only handles `/` and `/home` and swap partitions. Some of installers (such as Debian installer) suggest having `/var` or `/tmp` as separate partitions as well. This will be fixed in a future update. (See [documents]() for more information.)

Now, you can enjoy the new experience of a live system installer which even works on a live disc! 