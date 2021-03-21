# Deploy ArgoCD

In the `argocd` directory, there are several yaml files that could be used to deploy an instance of ArgoCD.

This deployment uses the ArgoCD operator.

1. Create the namespace, named `argocd`
    ```
    oc apply -f argocd/namespace.yaml
    ````

1. Deploy the ArgoCD operator in the created namespace
    ```
    oc apply -f argocd/operator.yaml
    ````
    It creates an `OperatorGroup`, a subscriotpn to ArgoCD operator. It creates also a `clusterroleinding` to give priviliege to argocd to manage comopenents on the cluster.

1. Create an instance of ArgoCD
    ```
    oc apply -f argocd/argocd_instance.yaml

The ArgoCD instance is basic but it include the definition of a route allowing toa ccess ArgoCD console and the integration with OpenShift authentication (dex). 