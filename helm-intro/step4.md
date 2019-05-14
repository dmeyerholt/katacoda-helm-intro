Now lets examine what has happened:
We check the list of releases using `helm list`{{execute}}. Note the random
name of that released (could be overridden). The used
wordpress chart creates a bunch of kubernetes resources:
* See the created _deployments_ `kubectl get deployments`{{execute}},
* the created _Stateful Sets_ `kubectl get statefulsets`{{execute}},
* the started _pods_ of these resources `kubectl get pods`{{execute}},
* the created _config maps_ `kubectl get configmaps`{{execute}},
* the created _secret_ `kubectl get secrets`{{execute}} and
* the created _services_ `kubectl get svc`{{execute}}.

To see that it is really working we connect to the nodeport in order to reach the application:

https://[[HOST_SUBDOMAIN]]-30000-[[KATACODA_HOST]].environments.katacoda.com/

