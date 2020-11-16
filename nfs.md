# Definition of NFS componentes
RPC = Remote Procedure Calls, uses portmap underneath
rpc.mountd = receives mount requests and checks against the exported filesystem.
rpc.nfsd = user level parts of NFS. Provides additional threads for the NFS client to use.
rpc.statd = Implements the Network Status Monitor (NSM) RPC protocol. Reboot notification when NFS server is restarted without gracefull shutdown.

# SELinux and the use of NFS on home directories
* setsebool use_nfs_home_dirs on

# How to mount NFS on MacOS
mount -t nfs -o resvport,rw <server:/path/to/export> </path/to/mount>
