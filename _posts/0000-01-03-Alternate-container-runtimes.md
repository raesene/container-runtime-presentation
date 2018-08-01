# Alternate Container Runtimes

--

## "Standard Docker"

<img src="/images/docker.png"/>

--

## gVisor

<img src="/images/gvisor.png"/>

Note:

Lightweight, not a lot of resources, no need for "per app" configuration.  Userspace kernel written in go implements linux syscall.  Should be relatively light.  Used in things like Google App engine. gVisor then integrates with the "real" linux kernel.  Reduces attack surface. Doesn't implement all available syscalls (currently 211 of 319). Also some restrictions (e.g. no NET_RAW).  Also in any scenarios where things like namespaces would be shared, I don't think gVisor would work.

--

## Kata Containers

<img src="/images/kata-containers.png"/>

Note:

This project came out of a combination of 

--

## ContainerD

<img src="/images/containerd.png"/>

--

## LXD

<img src="/images/lxc-lxd.png"/>
