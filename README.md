# Using Gatekeeper mutation policy

### Deploy Gatekeeper on the TKGs cluster
IMPORTANT: Make sure you have admin access to the cluster 

Install the latest version of Gatekeeper - E.g.

```bash
kubectl apply -f https://raw.githubusercontent.com/open-policy-agent/gatekeeper/v3.14.0/deploy/gatekeeper.yaml
```

### Deploy the Metadata mutating policy
This policy will add a label `pod-security.kubernetes.io/enforce:privileged` to all new namespacres that get created. 

```bash
kubectl apply -f assignmetadata-psa.yaml
```
