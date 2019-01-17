My installation of unifi-controller based on Kubernetes.

This installation is inspired by the deployment found in the original Ubiquiti docker/kubernetes installation.
https://github.com/alias2696/Ubiquiti-Unifi-Controller
That implementation was a bit rude for my system and I had other issues, such as using NFS.
 
Please install https://raw.githubusercontent.com/google/metallb first for external (your lan) exposure.
Metallb fits perfectly for my personal k8s installation.

I use jacobalberty/unifi:latest as a container for the controller. This one seem to be well maintained.
I use mongo:latest as a container for the database.

- Files are stored on my synology nas via NFS. These are my personal settings. Change them to your needs.
- Change the loadBalancerIP values to match a free number in your lan (and in the designated ip space entered in Metallb).
- Change you unifi dns entry to match loadBalancerIP.
- unifi-controller and mongodb will be installed in the unifi namespace
- made an seperate pv for the mongodb nfs share. 

feel free to use my ideas, if it helps you, let me know.
feel free to use my ideas, if I can help you, let me know.


