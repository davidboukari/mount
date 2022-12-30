# mount

* Fat32
```
mkdir -p /tmp/disk
chown -R $USER.$USER /tmp/disk
mount -o user,uid=$USER /dev/sdb1 /tmp/disk
```


# hfsplus, hfs+
```
sudo mount -t hfsplus -o force,rw /dev/sda2 /media/hfsplus

The following steps is optional if you encounter file permission and not able to access particular folders or files. We will need bindfs

sudo apt install bindfs

Now take mounted file system before and provide a view of it with any uid you'd like.

mkdir ~/anyfolder
sudo bindfs -u $(id -u) -g $(id -g) /media/hfsplus ~/anyfolder

```
