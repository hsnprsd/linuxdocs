# Introduction

Notes taken while learning how Linux works.

# TOC

- [Processes](./processes/README.md)
- [IO Devices](./io/README.md)
- [Networking](./networking/README.md)
- [System Statistics](./sysstats/README.md)

# TODO

procs:
- systemd (systemctl / journalctl)
- top
- ps
- strace
- kernel mode vs. user mode

io-devices:
- raid (soft/hard)
- iotop
- SAN / NAS

networking:
- systemd-resolved
- netplan
- ss / netstat
- iperf / nethogs / iftop
- wireshark / tcpdump
- nmap (security)
- ip (route, link, addr)
- iptables
- network interfaces (deep dive)
- ping
- nc / telnet
- lsof
- QUIC
- TLS

filesystem:
- filesystems (ext4, xfs, tmpfs, btrfs, etc.)
- lsblk
- inodes
- fsck / cfdisk
- file descryptors
- lsof
- df / du
- find

virtualization:
- hypervisors (kvm / virtualbox / vagrant)
- emulators (qemu)

containerization:
- cgroups
- namespaces

terminals:
- pty / tty

text manipulation:
- sed
- awk

server administration:
- ILO
