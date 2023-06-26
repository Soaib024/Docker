# Containers from 30,000 feet

## The bad old days

In the past we could only run one application per server.
The open-systems world of Windows and Linux just didn’t have the technologies to safely and securely run multiple applications on the same server.
As a result, the story went something like this… Every time the business needed a new application, the IT department would buy a new server. 
Most of the time nobody knew the performance requirements of the new application, 
forcing the IT department to make guesses when choosing the model and size of the server to buy.

## Hello VMware!

Virtual machine (VM) allowed us to safely and securely run multiple business applications on a single server. 
IT departments no longer needed to procure a brand-new oversized server every time the business needed a new application, but
- Every VM requires its own dedicated operating system (OS) is a major flaw. 
- Every OS consumes CPU, RAM and other resources that could otherwise be used to power more applications
- VMs are slow to boot, and portability isn’t great
- Migrating and moving VM workloads between hypervisors and cloud platforms is harder than it needs to be.

## Hello Containers!

In the container model, the container is roughly analogous to the VM. A major difference is that containers do not require their own full-blown OS. In fact, all containers on a single host share the host’s OS

- Reduces the overhead of OS patching and other maintenance.
- Containers are also fast to start and ultra-portable.
- Moving container workloads from your laptop, to the cloud, and then to VMs or bare metal in your data center is a breeze.

## Linux containers

Some of the major technologies that enabled the massive growth of containers in recent years include; kernel namespaces, control groups, union filesystems, and of course Docker.

Despite all of this, containers remained complex and outside of the reach of most organizations. It wasn’t until Docker came along that containers were effectively democratized and accessible to the masses.mespaces, control groups, union filesystems, and of course Docker.

## Windows containers
The core Windows kernel technologies required to implement containers are collectively referred to as Windows Containers. The user-space tooling to work with these Windows Containers can be Docker.

## Linux vs windows vs mac container
 Running container shares the kernel of the host machine it is running on. This means that a containerized Windows app will not run on a Linux-based Docker host, and vice-versa.

 Windows container depending upon version of docker desktop might run either on top of Hyper-V VM or WSL and there is currently no such thing as Mac containers. However, we can run Linux containers on your Mac using Docker Desktop which runs containers inside of a lightweight Linux VM

 ## What about Kubernetes
 Kubernetes uses Docker as its default container runtime — the low-level technology that pulls images and starts and stops containers. However, Kubernetes has a pluggable container runtime interface (CRI) that makes it easy to swap-out Docker for a different container runtime. In the future, Docker might be replaced by containerd as the default container runtime in Kubernetes.

# Chapter Summary

We used to live in a world where every time the business wanted a new application we had to buy a brand-new server. VMware came along and enabled us to drive more value out of new and existing company IT assets. As good as VMware and the VM model is, it’s not perfect. Following the success of VMware and hypervisors came a newer more efficient and lightweight virtualization technology called containers. But containers were initially hard to implement and were only found in the data centers of web giants that had Linux kernel engineers on staff. Along came Docker, Inc. and suddenly containers were available to the masses.