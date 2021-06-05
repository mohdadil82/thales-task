# thales-task
start


Steps followed to compelete the task as below:
Task Completed as below:
- installed minikube & helm
- created empty repository in Git with name thales-task and cloned the Repo to the local drive
- created Kubernetes deployment with dedicated namespace (thales-task) into the folder thales-task
- updated service.yaml to change type of service to NodePort , calling from values.yaml
- updated replicacount=3 in values.yaml so we will have 3 pods available
- updated deployment.yaml to add spec for rolling update (max unavailbale=1)
- created API_KEY with the following commands and applied to namespace thales-task
  vi secret.yml 
  cp secret.yml thalesapikey.secret
  kubectl get secret
  kubectl apply -f thalesapikey.secret -n thales-task
  kubectl describe secret api-key -n thales-task
- called API_KEY under envi variables in deployment.yaml

