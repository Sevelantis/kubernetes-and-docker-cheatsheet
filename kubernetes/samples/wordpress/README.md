# Deploy WordPress on K3S

This tutorial shows you how to deploy a WordPress site and a MariaDB database using K3S.
Both services use images from [bitnami](https://bitnami.com/).
Both applications use PersistentVolumes and PersistentVolumeClaims to store data.

This tutorial uses 3 files:
1. **secrets** that has the credentials of the database and WordPress as a secret (the secret is encoded as BASE64)
2. **mariadb** the deployment of a single node for the database
3. **wordpress** a single deployment of a wordpress instance

**Note:** to try this deployment please change the namespace in all configuration files.

Run the following commands:
```bash
kubectl apply -f ./
kubectl get secrets -n prof
kubectl get pvc -n prof
kubectl get pods -n prof
kubectl get services -n prof
kubectl get ingress -n prof
```

Access the service through [here](wordpress-prof.k3s).

To remove the deployment simpy run:
```bash
kubectl delete -f ./
```
