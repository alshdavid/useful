Add this at the bottom of `/etc/samba/smb.conf`

```
[storage]
  path = /mnt/storage
  browsable =yes
  writable = yes
  guest ok = yes
  read only = no
  force user = nobody
```
