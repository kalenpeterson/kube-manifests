# kube-manifests
A Collection of Kubernetes Manifests

These are some examples of things I have gotten working and can use as a reference for manifests.

## Manifests
### apt-cacher-ng.yml
Creates a Deployment of apt-cacher-ng with a Service using NodePort 30142. Uses a hostPath Volume for persistant storage.

See: https://hub.docker.com/r/sameersbn/apt-cacher-ng

### docker-registry-proxy.yml
Creates a Deployment of docker-registry-proxy with a Service using NodePort 30128. Uses hostPath volumes for persistant storage.

Supports Authentication as ENV variables.

See: https://github.com/rpardini/docker-registry-proxy

### hellok8s-ingress-test.yml
Creates a Deployment of k8shello with a Service using a ClusterIP, and creates in ingress for ingress-nginx at /hello. Not persistant storage

### dashboard-ingress.yml
This is an example of how to use rewrite rules for services that require it. Kubernetes dashboard needs this, so I used it as an example.

### dnsutils.yml
Creates a Pod with dnsutils on the specified node. Usefull for troubleshooting. No persistant storage
