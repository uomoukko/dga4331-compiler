# dga4331-compiler
c/c++ compiler v14.2.0 for libc 2.27 to be used with DGA4331

if you cannot de-xz a tar.xz file on the modem, because your
tar is old and doesn't understand xz files, decompress it
in WSL linux with xz -d ct-ng-127REL-arm-arm-shortpath.tar<BR>
or in windows installing the 7-Zip utility, right-clicking
on the tar.xz file and selecting Extract to yourfile.tar
<BR>
format an usb disk as ext4 filesystem
If you have linux, sudo mkfs -t ext4 /dev/sda<BR>
If you have windows, you can use the free versions of DiskGenius<BR>
or MiniTool Partition Wizard<BR>
<BR>
mount the usb disk on a live-linux or windows-WSL-linux<BR>
create the directory m/opt on the mounted device<BR>
copy the ct-ng-127REL-arm-arm-shortpath.tar file on /m/opt<BR>
you can also extract the tar (tar xvf ct-ng-127REL-arm-arm-shortpath.tar)<BR>
<BR>
now mount the usb disk on the modem (remove noexec option)<BR>
as /chroot/tmp/run/mountd/sda1 type ext4 (rw,relatime,data=ordered)<BR>
go to directory /chroot/tmp/run/mountd/sda/m/opt<BR>
cd to /chroot/tmp/run/mountd/sda/m/opt
if you didn't do previously, extract the tar (tar xvf ct-ng-127REL-arm-arm-shortpath.tar)<BR>
<BR>
now everything is ok. Just add the compiler binaries to the path editing .profile<BR> PATH=$PATH:/usr/local/bin/:/chroot/tmp/run/mountd/sda1/m/opt/arm-unknown-linux-gnueabi/bin/<BR>
try the compiler typing gcc -v<BR>
