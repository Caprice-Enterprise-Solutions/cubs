# Introduction

In this documentations, you will learn how to use _Caprice Unified Base System_ or _CUBS_ to install a _Caprice Enterprise Linux_ system. For future references, we'll call the operating system _CEL_ and the installer _CUBS_. 

## What's is _Caprice Unified Base System_ ?

__CUBS__ is a backend for a live system installer. Mostly inspired by `pc-sysinstall` (from PC-BSD and TrueOS projects) and installers from older versions of Slackware or Arch Linux. 

CUBS simply takes a partitioned hard drive and some basic information such as a username for an administrator user account and your timezone, and copies the whole content of the live disc to your hard disk. 

It also can handle the bootloader installation for BIOS (UEFI support will be added in future releases.). 

The whole attempt at coding this piece of software is preparing an easy-to-use terminal based installer for live discs. 

## How to read this documentation 

Just go to the [Table of Contents](CONTENTS.md) and start reading there. We tried to keep everything straight forward. 