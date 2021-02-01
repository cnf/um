# namespaces -- k8s namespaces
{:data-section="k8s"}
{:data-date="June 26, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

Commands related to namespaces

## Resources

  * https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/

## Commands

`kubectl -n namespace-A get secret mysecret --export -o yaml |kubectl -n namespace-B apply -f -`
: Copy a secret from namespace-A to namespace-B
