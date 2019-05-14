Now we upgrade an existing charts and override the default value of `favorite.drink`: `helm upgrade demo demochart/ --set favorite.drink='Blood wine'`{{execute}}

Once again inspect the generated configmap
`kubectl get configmap demo-valuetests -o yaml`{{execute}}

As you can see, the configmap has been updated in-place. 