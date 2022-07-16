# Attach nfs server to k3s with smb sci driver with persistence volume

### About
This driver allows Kubernetes to access [SMB](https://wiki.wireshark.org/SMB) server on both Linux and Windows nodes, csi plugin name: `smb.csi.k8s.io`. The driver requires existing and already configured SMB server, it supports dynamic provisioning of Persistent Volumes via Persistent Volume Claims by creating a new sub directory under SMB server.

### Container Images & Kubernetes Compatibility:
|Driver Version | supported k8s version | supported [Windows csi-proxy](https://github.com/kubernetes-csi/csi-proxy) version |
|---------------|-----------------------|-------------------------------------|
|master branch  | 1.20+                 | v0.2.2+                             |
|v1.8.0         | 1.20+                 | v0.2.2+                             |
|v1.7.0         | 1.20+                 | v0.2.2+                             |
|v1.6.0         | 1.20+                 | v0.2.2+                             |

### Helm Chart

Repo: https://github.com/kubernetes-csi/csi-driver-smb/tree/master/charts/v1.8.0/csi-driver-smb

**Helm install**

```bash
export namespace="smb-csi-driver"

suo kubectl create namespace 
helm install csi-driver-smb csi-driver-smb/csi-driver-smb/v1.8.0 --namespace ${namespace}
```

### Create PV and PVC
TODO


### Create testing pod
TODO

