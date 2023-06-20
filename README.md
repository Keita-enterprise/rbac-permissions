# rbac-permissions
# use these commands when you are working in kubernete
| Commands | Description | Reference links |
|----------|-------------|------------------|
kubectl config get-contexts | List the name of all the clusters present | [ref](https://killercoda.com/killer-shell-cka/scenario/rbac-user-permissions) |
 k -n applications create role smoke --verb create,delete --resource pods,deployments,sts| This will create a role and add differents verbs | -----|
 kubectl -n applications create rolebinding smoke --role smoke --user smoke| This will create a rolebinding called smoke for role smoke and user smoke|
 k -n applications create rolebinding smoke-view --clusterrole view --user smoke| This allow Smoke ussers to view resources | ------|
 k auth can-i create deployments --as smoke -n applications| This will check the permission|----|
 kubectl whoami --show-identity| command to list users| ----|

