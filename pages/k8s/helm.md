# helm -- The package manager for Kubernetes
{:data-section="k8s"}
{:data-date="August 26, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

Helm is the best way to find, share, and use software built for Kubernetes.

## REFERENCES

* https://helm.sh/docs/using_helm/

## COMMANDS

`helm ls --all`
: List releases

`helm install --name <releasename> --namespace <namespace> -f values.yaml <packagename>`
: install package \<packagename\> with \<releasename\> into \<namespace\>, using values.yaml

`helm upgrade -f values.yaml <releasename> <packagename>`
: Upgrade a release with new values, and/or a new package

`helm show values <packagename>`
: Show the default values for \<packagename\>
