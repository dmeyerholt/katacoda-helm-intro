Now for something funny: We install a second release of the same chart. This time we specify a name for the new release:

`helm install stable/wordpress --name second --set service.type=NodePort,persistence.enabled=false,mariadb.master.persistence.enabled=false`{{execute}}

again check the created resources this time using `kubectl get all`{{execute}}


