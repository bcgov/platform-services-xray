# JFrog Xray

## What am I?

This repo is for the Xray image scanning tool for Artifactory.

## Contact Info

For help and support, check out the #devops-artifactory channel on Rocketchat!

## Vendor Info

Xray is a Jfrog product.


## How to Install

```
ocas apply -f quotas/compute-long-running.yaml
ocas apply -f quotas/storage.yaml
ocas apply -f storage-netapp-file-standard.yaml
helm upgrade --install xray jfrog/xray -f helm-values-lab.yaml
```
