# TCP-PLB

Protective Load Balancing (PLB) is a host based load balancing mechanism
for data center networks developed at Google. PLB builds on top of ECMP
which is the de facto standard mechanism to map flows to egress links in
data center networks. On a high level, PLB senses congestion and upon
meeting a threshold, makes the TCP connection probabilistically switch
to a different path in the network. More details about PLB are
available in SIGCOMM 2022 paper:
  https://doi.org/10.1145/3544216.3544226

# Open Source Details

TCP-PLB was added to open source BBR repository in v2alpha branch with
the following commit

https://github.com/google/bbr/commit/cf9b1dacabb1ef62481a452f7f169e1679e2da49

More details on how to compile and run the kernel can be found in the
v2alpha branch documentation

https://github.com/google/bbr/tree/v2alpha

#
