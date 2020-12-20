# Practical use of Kubernetes Volume Snapshots
December 19th, 2020  
__Author:__ Grant Griffiths, Engineer @ Pure Storage and Kubernetes-CSI contributor

## Overview

With the release of Kubernetes 1.20, [Volume Snapshot support is now GA](https://kubernetes.io/blog/2019/12/09/kubernetes-1-17-feature-cis-volume-snapshot-beta/)! In this post, we will cover how this feature can be used in practice by end users and external systems via the the VolumeSnapshot client. 

To use volume snapshots, make sure your Kubernetes 1.17+ cluster has met the following requirements:

1. [Volumesnapshot Beta or GA CRDs](https://github.com/kubernetes-csi/external-snapshotter/tree/24a2aa84366248fbdfae9660dd3a768c57971605/client/config/crd) installed
2. [Snapshot controlled installed](https://github.com/kubernetes-csi/external-snapshotter/tree/24a2aa84366248fbdfae9660dd3a768c57971605/deploy/kubernetes/snapshot-controller)
3. [CSI Driver(s) with Volume Snapshot support](https://kubernetes-csi.github.io/docs/drivers.html). The concepts in this blog have been tested with the DigitalOcean, Openshift-Storage, Pure Storage Orchestrator, and Portworx CSI drivers.

## Taking snapshots

To take a volume snapshot, the user must create a `VolumeSnapshot` object:

```

```

## Restoring a PVC

### References
1. https://kubernetes.io/blog/2020/12/10/kubernetes-1.20-volume-snapshot-moves-to-ga/
2. https://kubernetes.io/blog/2019/12/09/kubernetes-1-17-feature-cis-volume-snapshot-beta/
