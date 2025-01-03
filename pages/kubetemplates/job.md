# Job

    apiVersion: batch/v1 
    kind: Job 
    metadata: 
      name: JOBNAME 
      namespace: NAMESPACE 
    spec: 
      template: 
        spec: 
          securityContext: 
            runAsUser: 1000 
            fsGroup: 100
          containers: 
            - name: CONTAINERNAME
              image: IMAGE 
              ports: 
                - containerPort : 22 #ssh
              command: ["sleep"]
              args: ["infinity"]
              volumeMounts: 
               - name: nfs 
                 mountPath: "/mnt/nfs"
              resources: 
                requests: 
                  cpu: CPU 
                  memory: MEMORYGi
                  nvidia.com/gpu: GPU 
                limits: 
                  cpu: CPU 
                  memory: MEMORYGi
                  nvidia.com/gpu: GPU
          volumes: 
            - name: nfs
              persistentVolumeClaims: 
                claimName: nfsclaim
          restartPolicy: Never
      backoffLimit: 1