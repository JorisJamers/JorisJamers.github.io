# Ingress

    apiVersion: networking.k8s.io/v1
    kind: Ingress
    metadata:
      name: INGRESSNAME
    spec:
      rules:
      - host: URL
        http:
          paths:
          - backend:
              serviceName: SERVICENAME 
              servicePort: SERVICEPORT 
