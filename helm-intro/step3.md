Quickly setup a wordpress instance using this one-liner.

`helm install stable/wordpress --set service.type=NodePort,service.nodePorts.http=30000,persistence.enabled=false,mariadb.master.persistence.enabled=false`{{execute}}

While this is running, we examine the documentation of a that specific chart here [Wordpress Chart](https://github.com/helm/charts/tree/master/stable/wordpress)

