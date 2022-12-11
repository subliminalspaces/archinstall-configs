We are now using archinstall.

First: 

```
sudo pacman -S archinstall
```
You can then:

```
sudo archinstall --guided
```
or

```
sudo archinstall --dry-run
```
This will create some default configs in /var/log/archinstall/
These configs are some good presets, but the generated configs might be helpful too.
Then:

```
Modify cred.json with your desired credentials
```

Then:

```
Modify config.json with your desired configs. Pay special attention to "bootloader", "filesystem", "gfx_driver", "packages", "harddrives", "nic", and "profile".
```

Then:
```
Modify disk-layouts.json. Take special care with this file. You can seriously screw your system up.
Make sure that every hard drive in "harddrives":[] in config.json has a configuration in this file.
```

Then:

```
arch-chroot
```

Check and make sure you can 
```
ping archlinux.org
```
Then exit chroot
```
exit
```
and
```
sudo shutdown now
```
and finally.
```
boot up, and log in as new user.
```
And then follow the postinstall scripts to create some nice defaults.
