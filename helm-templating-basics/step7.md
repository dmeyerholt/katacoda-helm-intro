As `Blood wine` was mission-critical, we will revert the release to an older revision. Double check the revision history with `helm history demo`{{execute}}. 

Issue the helm rollback command: `helm rollback demo 2`{{execute}} and check the deployment again `helm get demo`{{execute}}. Issue `helm history demo`{{execute}} and now we see a new revision 4 with the note, that we rolled back. Blood Wine and Gagh. But we wanted Targ instead. 

To change helms behaviour in order to preserve existing value changes (We want Blood Wine) we issue the helm upgrade command again but instruct helm to keep our existing value change:

`helm upgrade demo demochart/ -f values-qonos.yaml --reuse-values`{{execute}}
