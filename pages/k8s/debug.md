# debuging -- debugging tips and tricks
{:data-section="k8s"}
{:data-date="July 15, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS


## DESCRIPTION


## COMMANDS

`kubectl describe TYPE NAME_PREFIX`
: Print a detailed description of the selected resources, including related resources such as events or controllers. You may select a single object by name, all objects of that type, provide a name prefix, or label selector.

`kubectl get events -n kube-system`
: print system events

