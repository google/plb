# PLB

Protective Load Balancing (PLB) is a host based load balancing mechanism
for data center networks developed at Google. PLB builds on top of ECMP
which is the de facto standard mechanism to map flows to egress links in
data center networks. On a high level, PLB senses congestion and upon
meeting a threshold, makes the TCP connection probabilistically switch
to a different path in the network. More details about PLB are
available in SIGCOMM 2022 paper:
  https://doi.org/10.1145/3544216.3544226

# TCP-PLB Open Source

TCP-PLB is open source with two implementation flavors.

## Linux Upstream

PLB support for TCP has been merged into net-next and is slated to be in
Linux v6.2. Additionally, PLB is hooked up to DCTCP but is disabled by
default. net-next commit URLs are listed below

https://git.kernel.org/pub/scm/linux/kernel/git/netdev/net-next.git/commit/?id=bd456f283b66
https://git.kernel.org/pub/scm/linux/kernel/git/netdev/net-next.git/commit/?id=1a91bb7c3ebf
https://git.kernel.org/pub/scm/linux/kernel/git/netdev/net-next.git/commit/?id=c30f8e0b0480
https://git.kernel.org/pub/scm/linux/kernel/git/netdev/net-next.git/commit/?id=29c1c44646ae
https://git.kernel.org/pub/scm/linux/kernel/git/netdev/net-next.git/commit/?id=29c1c44646ae

For more information on how to enable PLB, either consult the PLB paper or lookup the sysctl
documentation under //Documentation/networking/ip-sysctl.rst

## BBR Open Source Repo

TCP-PLB was added to open source BBR repository in v2alpha branch with
the following commit

https://github.com/google/bbr/commit/cf9b1dacabb1ef62481a452f7f169e1679e2da49

More details on how to compile and run the kernel can be found in the
v2alpha branch documentation

https://github.com/google/bbr/tree/v2alpha

# Contact

Please email plb-contact@google.com with any queries
