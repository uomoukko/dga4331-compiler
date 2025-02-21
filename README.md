# dga4331-compiler
c/c++ compiler v14.2.0 for libc 2.27 to be used with DGA4331

insert an ext4 formatted device, mount it (remove noexec option)<BR>
/chroot/tmp/run/mountd/sda1 type ext4 (rw,relatime,data=ordered)<BR>
create a directory /chroot/tmp/run/mountd/sda/m/opt<BR>
cd to /chroot/tmp/run/mountd/sda/m/opt<BR>
extract the compiler (tar xvaf ct-ng-127REL-arm-arm-shortpath.tar.xz)<BR>
edit .profile:PATH=$PATH:/usr/local/bin/:/chroot/tmp/run/mountd/sda1/m/opt/arm-unknown-linux-gnueabi/bin/<BR>
try the compiler typing gcc -v<BR>
