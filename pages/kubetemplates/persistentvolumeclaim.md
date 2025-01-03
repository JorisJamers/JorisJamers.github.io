# Persistent Volume Claim

  apiVersion: v1
  kind: PersistentVolumeClaim
  metadata:
    name: pvcname
    namespace: NAMESPACE
  spec:
    accessModes:
      - "ReadWriteMany"
    resources:
      requests:
        storage: "5Gi"
    storageClassName: nfsdirectmount
    volumeName: volumename
