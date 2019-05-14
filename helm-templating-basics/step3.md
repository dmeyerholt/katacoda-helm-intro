This scenario has a very small chart prepared in the folder `demochart`

Install a release of it using

`helm install --name demo demochart/`{{execute}}

check successful install using
`helm ls`{{execute}}

have a look at the generated configmap using
`kubectl get configmap demo-valuetests -o yaml`{{execute}}

You will note in the `data` key the values of `food`, `drink` and `staticvalue`. in the editor pane examine, why it is like that:
* the `values.yaml` defines the values of food and drink
* the `templates/config.yaml` contains the template for the configmap
* In the template note the usage of some default helm values as well as the usage of specific values defined in the `_helpers.tpl` file which is always included while rendering the manifest
