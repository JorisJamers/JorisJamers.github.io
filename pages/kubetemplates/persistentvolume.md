# Persistent Volume

## NFS storageclass

    apiVersion: v1
    kind: PersistentVolume
    metadata:
      name: volumename
    spec:
      capacity:
        storage: 5Gi
      volumeMode: Filesystem
      accessModes:
        - ReadWriteMany
      persistentVolumeReclaimPolicy: Retain
      storageClassName: nfsdirectmount
      mountOptions:
        - nfsvers=3
      nfs:
        path: /path/to/folder/on/server
        server: NFS_SERVER
