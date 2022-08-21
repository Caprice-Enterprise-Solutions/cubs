# Installation Process

In the [previous part](PREPARATIONS.md) we've found out how to login into a new CEL installation session and also prepare our hard drive for a clean and fresh installation. In this part of the documentation, we're going to understand how CUBS actually works and how we can do the best installation process possible!

## Partition scheme 

For more accuracy in the process of installation, let's review our partitions. We had these: 

- `/dev/vda1` for _swap_. 
- `/dev/vda2` for _root_. 
- `/dev/vda3` for _home_. 

Now, we need to understand how CUBS understands these partitions.

## Installation parameters

### Required parameters

- `--root` : You need to define a root partition. CUBS makes a filesystem with `ext4` format on the destination partition. It needs to be defined, otherwise there'll be no place to install your CEL session. 
- `--bootloader` : You need to define the main hard disk with this flag. It's necessary because it install GRUB on your selected disc. 
- `--username` : You need to define a username for the administrator account. It usually is root, but for some security reasons, we don't suggest logging in with root. Instead, you can create an account who's a member of `sudo` group to do admin things!
- `--password` : The password for the administrator account. Be careful when you use this, because the password can be seen when you run CUBS on a terminal. 

So, the installation process will be : 

```
:~# cubs --root /dev/vda2 --bootloader /dev/vda --username YOUR_CHOSEN_USERNAME --password YOUR_CHOSEN_PASSWORD

``` 

### Recommended parameters

- `--home` : You can define a home partition with this. We have chosen a home partition, so we're going to use this at the end of this section. 
- `--swap` : You can define the swap area using this flag. 
- `--timezone` : You can define the timezone using this flag easily. 

## Examples 

### Only root partition 

```
:~# cubs --root /dev/vda2 --bootloader /dev/vda --username YOUR_CHOSEN_USERNAME --password YOUR_CHOSEN_PASSWORD

``` 

### Adding the swap area
```
:~# cubs --root /dev/vda2 --swap /dev/vda1 --bootloader /dev/vda --username YOUR_CHOSEN_USERNAME --password YOUR_CHOSEN_PASSWORD

``` 

### Using a separate _/home_ partition 

```
:~# cubs --root /dev/vda2 --swap /dev/vda1 --home /dev/vda3 --bootloader /dev/vda --username YOUR_CHOSEN_USERNAME --password YOUR_CHOSEN_PASSWORD

``` 

P.S : You can do this without ```--swap``` as well. 

### Giving a chosen time zone

For instance, we are going to set our time zone on _Asia/Tehran_. 

```
:~# cubs --root /dev/vda2 --swap /dev/vda1 --home /dev/vda3 --bootloader /dev/vda --username YOUR_CHOSEN_USERNAME --password YOUR_CHOSEN_PASSWORD --timezone Asia/Tehan

``` 

P.S : You can do this without `--swap` or `--home` as well.
