#  Deploy Rundeck Open Source on Kubernetes

Deploy a Rundeck on Kubernetes, ready to run jobs on it.

Rundeck version: 4.3.1
Database: local (H2)  # H2 database is recommended only for development and testing

is a workable architecture that can easily be used as a basis for deploying a fully HA production Rundeck cluster.

## 🚀 Quick start

If you have helm, you can deploy with the folling command:
```
helm upgrade --install rundeck-main rundeck-main \
  --repo https://github.com/dgolive/rundeck-helm \
  --namespace rundeck-main --create-namespace
```
It will install the Rundeck in the rundeck namespace, creating that namespace if it doesn't already exist.

### Access Rundeck WebUI 

Open a web browser if your preference and try out:

```
http://localhost:4440

Login: admin
Password: admin
```
## Uninstall

```
helm uninstall -n rundeck rundeck
```
