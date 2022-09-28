# Installation of Let's Encrypt Wildcard SSL Certificate on VKE cluster

The following are the prerequisites and the steps to install a wildcard SSL certificate issued by Let's Encrypt on a VKE cluster.

## Prerequisites
* Deploy a server with Ubuntu 22.04 - [link](https://my.vultr.com/)
* Deploy a VKE cluster - [link](https://my.vultr.com/kubernetes/)
* Create a new DNS zone - [link](https://my.vultr.com/dns/)

## Command Line Tools
* Install Kubectl - [installation link](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-kubectl-binary-with-curl-on-linux)
* Install Helm - [installation link](https://helm.sh/docs/intro/install/#from-script)

## Kubernetes Plugins
* Install ExternalDNS configuration for Vultr DNS - [manifest file link](/01-dns.yaml)
* Install nginx-ingress controller - [installation link](https://kubernetes.github.io/ingress-nginx/deploy/#quick-start)
* Install cert-manager plugin - [installation link](https://cert-manager.io/docs/installation/)
* Install Vultr webhook for cert-manager plugin - [installation link](https://github.com/vultr/cert-manager-webhook-vultr) | [manifest file link](/02-webhook.yaml)

## Kubernetes Resources
* Create a wildcard SSL certificate - [manifest file link](/03-certificate.yaml)
* Create a nginx deployment - [manifest file link](/04-nginx.yaml)
* Create an ingress reseource - [manifest file link](/05-ingress.yaml)
