# zoneddevicesHDDSSDs





Setting-up a Zoned Storage Compatible Linux System
------------------------------------------------------
```
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ uname -r
5.17.5-300.fc36.x86_64
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ cat /boot/config-`uname -r` | grep CONFIG_BLK_DEV_ZONED
CONFIG_BLK_DEV_ZONED=y
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
```




Zoned Block Device Emulation
------------------------------------------------------


```
[zonednamespacezns@localhost-live ~]$ modprobe null_blk nr_devices=1 zoned=1
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ sudo blkzone report /dev/nullb0
[sudo] password for zonednamespacezns: 
  start: 0x000000000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000080000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000100000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000180000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000200000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000280000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000300000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
  start: 0x000380000, len 0x080000, cap 0x080000, wptr 0x000000 reset:0 non-seq:0, zcond: 1(em) [type: 2(SEQ_WRITE_REQUIRED)]
[zonednamespacezns@localhost-live ~]$ 
[zonednamespacezns@localhost-live ~]$ 
```






Getting Started with SMR Hard Disks
------------------------------------------------------



Getting Started with NVMe ZNS Devices
------------------------------------------------------
