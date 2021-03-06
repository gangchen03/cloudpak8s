# GuestBook Example with kube resource
This example is trying to convert k8s guest book example [https://kubernetes.io/docs/tutorials/stateless-application/guestbook] into mcm application

Following 1 chart is for mcm-application
1. gbapp

## What's New
1. Use Kube resource directly in deployable

## Usage
0. Clone the repo, package app charts with ```helm package gbapp```
1. Load application charts into ICP with ```cloudctl catalog load-chart --archive gbapp-0.1.0.tgz```
2. Install application chart with GUI or CLI ```helm install gbapp -n <release-name> --tls ```
3. Update placement related values to redeploy application
4. Delete helm release to deregister application ```helm delete <release-name> --purge --tls```
