# kubectl -- Controll k8s clusters
{:data-section="shell"}
{:data-date="May 30, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

Do things with kubectl

## References

  * https://kubernetes.io/docs/reference/kubectl/overview/
  * https://kubernetes.io/docs/reference/kubectl/cheatsheet/

## Commands

### Config file
`kubectl config view`
: Show Merged kubeconfig settings.

`KUBECONFIG=~/.kube/config:~/.kube/kubconfig2`
: Use multiple kubeconfig files at the same time and view merged config

`kubectl config view`
: Show config content.

### Context

`kubectl config get-contexts`
: Display list of contexts.

`kubectl config current-context`
: Display the current-context.

`kubectl config use-context my-cluster-name`
: Set the default context to my-cluster-name

`kubectl config set-context gce --user=cluster-admin --namespace=foo && kubectl config use-context gce`
: Set a context utilizing a specific username and namespace.

`kubectl config set-context --current --namespace=ggckad-s2`
: Permanently save the namespace for all subsequent kubectl commands in that context.

### User Management
`kubectl config view -o jsonpath='{.users[?(@.name == "e2e")].user.password}'`
: Get the password for the e2e user.

`kubectl config view -o jsonpath='{.users[].name}'`
: Get a list of users.

`kubectl config set-credentials kubeuser/foo.kubernetes.com --username=kubeuser --password=kubepassword`
: Add a new user that supports basic auth.

`kubectl config unset users.foo`
: Delete user foo.

### Clusters

`kubectl config --kubeconfig=config-demo set-cluster development --server=https://1.2.3.4 --certificate-authority=fake-ca-file`
: Add cluster details to your configuration file.

