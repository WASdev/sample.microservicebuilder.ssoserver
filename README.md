# Microservice Sample - single sign on service

See the [sample documentation](https://github.com/WASdev/sample.microservices.docs) for more information.

Update the value of EXTERNAL_IP_ADDR in chart/ssoserver/templates/ipaddr-config.yaml to be the IP address of the external ingress for your Kubernetes cluster before deploying this chart. 

To rebuild the username/password data, 
  ```
  kubectl create secret generic liberty-userids --dry-run -o yaml --from-file="userids.xml" >! chart/ssoserver/templates/deploy-ssoservice.yaml
  ```



