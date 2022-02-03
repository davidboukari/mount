# mount

* Fat32
```
mkdir -p /tmp/disk
chown -R $USER.$USER /tmp/disk
mount -o user,uid=$USER /dev/sdb1 /tmp/disk
```
