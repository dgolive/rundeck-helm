#  Deploy Rundeck on Kubernetes

## About Rundeck

Rundeck is an open source automation service with a web console, command line tools and a WebAPI. It lets you easily run automation tasks across a set of nodes.

This documentation describes how to deploy Rundeck Open Source on Kubernetes and ready to run jobs on it.

Versions:
- Rundeck version: 4.3.1
- Database: H2 local
- Kubernetes: 1.24

*H2 database is recommended only for development and testing.


## Quick start 🏁

Deploy with the following helm command:
```
helm upgrade --install rundeck rundeck \
  --repo https://dgolive.github.io/rundeck-helm/ \
  --namespace rundeck --create-namespace
```
It will install the Rundeck in the rundeck namespace, creating that namespace if it doesn't already exist.


## Access Rundeck 🚀 

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


## References ⛏️
- https://www.rundeck.com
- https://docs.rundeck.com/docs/
- https://github.com/rundeck/rundeck
- https://github.com/rundeck/docker-zoo/tree/master/kubernetes

