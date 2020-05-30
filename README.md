kubectl get all -n databases
kubectl delete pods rabbitmq-rabbitmq-ha-0 -n databases
kubectl port-forward svc/prometheus-operator-prometheus -n monitoring 6900:9090 
gcloud container clusters get-credentials loopr-dev-cluster --region us-central1 --project=inviz-falcon-dev
 gcloud auth activate-service-account --key-file=/home/asutosh/Downloads/deployment-sa.json --project=inviz-falcon-dev
kubectl logs -f rabbitmq-rabbitmq-ha-0 -n databases -c rabbitmq-ha-exporter
kubectl get svc -n databases
helm uninstall rabbitmq -n databases
kubectl get roles -n databases
kubectl delete roles/rabbitmq-rabbitmq-ha -n databases
kubectl get secrets -n databases
kubectl describe secrets/db-user-pass
kubectl get secret mysecret -o yaml
kubectl delete secret ssl-key-cert
kubectl delete configmap <configmap-name> -n <namespace-name>
kubectl get pods -o wide
kubectl describe nodes my-node
kubectl describe pods my-pod
kubectl scale --current-replicas=2 --replicas=3 deployment/mysql
kubectl delete pod,service baz foo                                        # Delete pods and services with same names "baz" and                                                                                                                           "foo"
kubectl delete pods,services -l name=myLabel
kubectl logs -f my-pod                              # stream pod logs (stdout)
kubectl logs -f my-pod -c my-container 
kubectl exec my-pod -- ls /                         # Run command in existing pod (1 container case)
kubectl exec my-pod -c my-container -- ls /         # Run command in existing pod (multi-container case)
kubectl apply -f ./my-manifest.yaml 




