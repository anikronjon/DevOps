# AWS EC2


### AWS EBS (Elastic Block Storage)
- Volumes
- Snapshots
- Lifecycle Manager

**Volumes:** We can create EBS volume, attach and detach to instance as well as modify(increase) it.


### Add/mount a new volume to an instance.

First create a new volume and atach it to an instance.
**NOTE:** Makesure the *availability zone* of the volume will be same as the instance
```shell
# Check volume, partision, mountpoint in an instance
    $ sudo lsblk
2. Check specific volume weather filesystem available or not
	$ sudo file  -s /dev/_volume_

3. Add a filesystem to that volume
	$ sudo mkfs.ext4 /dev_volume_

4. Mount the volume to this instance
	$ sudo mkdir /_dirname_ ; sudo mount /dev/_volume_  /_dirname_
```


### Modify/Increase the volume size of extra mounted volume

First to increase the volume size *select the instance > Actions > Modify Volume > Modify*

**NOTE:** Make sure the *volume type* must match with instance type(**NITRO, XEN**), like gp2 is xen type on the contary gp3 is nitro type.
```
1. Check volume, partision, mountpoint in an instance
	$ sudo lsblk

2. Check The device filesystem is same as partision
	$ sudo df -s

3. Resize the Filesystem
	# ext2, ext3, ext4 filesystem
	$ sudo resize2fs /dev/_volume_
	# for xfs filesystem
	$ sudo xfs_growfs /dev/_volume_
```