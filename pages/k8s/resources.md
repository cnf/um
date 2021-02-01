# resources -- API endpoints
{:data-section="k8s"}
{:data-date="October 15, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS


## DESCRIPTION

`kubectl api-resources`
: List all supported resource types along with their shortnames, API group, whether they are namespaced, and Kind:


Other operations for exploring API resources:

`kubectl api-resources --namespaced=true`
: All namespaced resources

`kubectl api-resources --namespaced=false`
: All non-namespaced resources

`kubectl api-resources -o name`
: All resources with simple output (just the resource name)

`kubectl api-resources -o wide` 
: All resources with expanded (aka "wide") output

`kubectl api-resources --verbs=list,get`
: All resources that support the "list" and "get" request verbs

`kubectl api-resources --api-group=extensions`
: All resources in the "extensions" API group
