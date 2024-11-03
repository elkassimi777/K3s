K3s Setup Guide
In this repository, I will outline all the steps to set up a K3s Kubernetes cluster.

Overview
This setup will demonstrate how to configure a K3s cluster with:

One master node: Your local computer
One worker node: A Raspberry Pi device
The guide will take you through each step to connect these nodes into a functional Kubernetes cluster.


- Installing K3s server:
    curl -sfL https://get.k3s.io | sh -
    After the installation to very K3s kubectl get nodes to show nodes in the cluster

- Installing  K3s agent
   before the installation you need need to get the master node ip address andd token
   stored in this path : /var/lib/rancher/k3s/server/node-token

   Then we install K3s on the worker node : curl -sfL https://get.k3s.io | K3S_URL=https://<server-ip>:6443 K3S_TOKEN=<node-token> sh -
