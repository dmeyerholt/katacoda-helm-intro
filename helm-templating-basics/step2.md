As we have a naked kubernetes cluster, we need to initialize helm on the client as well as on the cluster itself. This is accomplished by

`helm init`{{execute}}

Afterwards check the state of deployments and wait until all deployments have at least one available pod:

`kubectl get deployments --all-namespaces`{{execute}}
