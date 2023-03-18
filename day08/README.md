# AWS EC2


### AWS EBS (Elastic Block Storage)
- Volumes
- Snapshots
- Lifecycle Manager

**Volumes:** We can create EBS volume, attach and detach to instance as well as modify(increase) it.


### Add a new volume to an instance.
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