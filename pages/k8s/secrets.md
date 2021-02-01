# secrets -- k8s secrets
{:data-section="k8s"}
{:data-date="July 15, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

Kubernetes secret management

## DOCUMENTATION

https://kubernetes.io/docs/concepts/configuration/secret/

## COMMANDS

`kubectl create secret generic db-user-pass --from-file=./username --from-file=./password`
: Create a generic secret named *db-user-pass* with field *username* and *password* from files

`kubectl -n <namespace> describe secret $(kubectl -n <namespace> get secret | grep <service-account> | awk '{print $1}') | grep '^token:' | awk '{print $2}'`
: Get the token for a \<service-account\> in \<namespace\>
