### Pre-requisites
1. Azure keyvault 
1. Azure application with access to the keyvault secrets

### Setup

1. Install ESO with helm
    ```
    helm repo add external-secrets https://charts.external-secrets.io

    helm install external-secrets \
        external-secrets/external-secrets \
        -n external-secrets \
        --create-namespace \
        --version 0.16.0
    ```

1. (Optional) Deploy secret zero for ESO to use to connect to azure secret store
    ```
        kubectl apply -f secret-zero.yaml
    ```