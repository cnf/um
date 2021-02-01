# dashboard -- Show the k8s dashboard
{:data-section="k8s"}
{:data-date="June 26, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

How to do k8s stuff on azure with az

## Tasks

`az aks browse -n cotarch -g cotarch --disable-browser`
: Open the k8s dashboard, but don't open the dashboard.

`kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep kubernetes-dashboard | awk '{print $1}') | grep '^token:' | awk '{print $2}'`
: Get a token for the dashboard



## OPTIONS

