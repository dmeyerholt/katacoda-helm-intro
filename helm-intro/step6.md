Examine the deployment of the second wordpress:
`kubectl describe deployment second-wordpress`{{execute}}
note how all relevant sections are prefixed using the release name. 

Before we go further into detail regarding the rendering of templates,
clean up your releases again using 
`helm delete second`{{execute}} do this again for your first release. Please not that the release name of the first release is randomly generated so first look up the name of the release.

Now after removing we check again all our resources `kubectl get all`{{execute}} hopefully all should be empty (except the kubernetes service).
