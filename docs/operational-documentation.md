# Operational Documentation

How do I install this application? How does the pipeline work? What external requirements does this app have?

Document the automation surrounding this app, like backups and storage notifications.

During the initial phase of development, you probably don't have this information, so it might be a good idea to use this document as a to-do list.

## Installation

Like this: 

```bash
helm template xray --namespace devops-xray -f helm-values-lab.yaml jfrog/xray > manifest.yaml
sed -i '' '/securityContext/d' ./manifest.yaml
sed -i '' '/runAsUser/d' ./manifest.yaml
sed -i '' '/fsGroup/d' ./manifest.yaml
sed -i '' '/allowPrivilegeEscalation/d' ./manifest.yaml
oc apply -f manifest.yaml
```

