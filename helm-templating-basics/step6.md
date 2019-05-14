Check the contents of `values-qonos.yaml` in the editor pane. Edit it to override not drink, but set food to `targ`. _hint_: You do not need to save in katacoda's editor pane. it saves on-the-fly.

Remember: Our current configmap contains: `drink=Blood Wine` and `food=gagh`. 

Now we upgrade our demo release again but supplying our changed values from the yaml-file:
`helm upgrade demo demochart/ -f values-qonos.yaml`{{execute}}

The output of the rendered NOTES.txt notifies us, that the contents of the configmap now states `drink` as `raktajino` and `food` as targ. 
So far so good. But why is `drink` reverted again to `raktajino`?

