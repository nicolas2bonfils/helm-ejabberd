# ejabberd

An Helm chart to deploy [ejabberd](https://github.com/processone/ejabberd)

## Goal

This repo contains an helm chart to help deploying ejabberd on Kubernetes cluster.
It uses the [official docker image](https://github.com/processone/docker-ejabberd/tree/master/ecs).

## Installation

### Namespace

Create a namespace for the app :

```shell
$ kubectl create ns ejabberd
```

### App

Currently that helm-chart is not (yet) deployed to a helm-registry. So you have to install it by checking out this repo

```shell
$ git checkout https://github.com/nicolas2bonfils/helm-ejabberd.git
$ cd helm-ejabberd
$ helm install -n ejabberd ejabberd . -f values.yaml
```

## Credits

The startup script ([`cluster.sh`](https://github.com/nicolas2bonfils/helm-ejabberd/blob/master/files/cluster.sh)) is from [Robbilie](https://github.com/Robbilie/kubernetes-ejabberd) repo.
