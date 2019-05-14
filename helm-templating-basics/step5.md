Look again at the status of the installed release `demo` using `helm ls`{{execute}}

As you can see, the _revision_ of the `demo` release has increased to revision 2. helm keeps track of all revisions of the releases it manages. you can get an overview of the history using `helm history demo`{{execute}}.

Now in more detail: use `helm get demo`{{execute}} to get insight of the current revision of the demo chart. Furthermore you can just get the changed values in `yaml`-format by using `helm get values demo`{{execute}}. lets save that output in an own values-files: `helm get values demo > values-qonos.yaml`{{execute}}. 



