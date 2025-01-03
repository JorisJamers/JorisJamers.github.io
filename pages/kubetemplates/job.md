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
            image: IMAGENAME
            ports:
                - containerPort: 8888 # jupyter
                - containerPort: 9001 # tensorboard
                - containerPort: 22 # ssh
            command: ["sleep", "infinity"]
            volumeMounts:
                - name: nfs
                mountPath: "/mnt/nfs"
            resources:
                requests:
                cpu: CPU
                memory: MEMORY
                nvidia.com/gpu: GPU
                limits:
                cpu: CPU
                memory: MEMORY
                nvidia.com/gpu: GPU
        volumes:
            - name: nfs
            persistentVolumeClaim:
                claimName: nfsclaim
        restartPolicy: Never
    backoffLimit: 1
