# pods --
{:data-section="k8s"}
{:data-date="August 13, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

Manipulating pods

## RESOURCES

  * https://kubernetes.io/docs/concepts/workloads/pods/pod/


## COMMANDS

`kubectl get pods | grep Evicted | awk '{print $1}' | xargs kubectl delete pod`
: Delete all Evicted (Failed) pods
