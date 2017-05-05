# Pipelines

```
oc new-project development --display-name="Development" --description="Development project"
oc new-app https://github.com/pblaas/simplephp-pipelines/blob/master/simplephp.build-dev.json
oc new-project testing --display-name="Testing" --description="Testing project"
oc new-app https://github.com/pblaas/simplephp-pipelines/blob/master/simplephp.build-test.json
oc new-project cicd --display-name="CICD" --description="CICD project"
oc policy add-role-to-user edit system:serviceaccount:cicd:jenkins -n testing
oc policy add-role-to-user edit system:serviceaccount:cicd:jenkins -n development

```
