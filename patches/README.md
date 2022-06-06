After the patch operator is installed and the correct permissions (via service account & cluster rolebinding) are granted, we can now create patches manifests so they are applied to the cluster.

Patches in this repo are as follows:

- Remove Self Provisioner role from all authenticated users. This prevents users from being able to create new namespaces / projects.
This is applied with the following:

oc apply -f selfprov-remove.yaml 

- Remove gp2 storageclass from being the default

oc apply -f gp2-default-sc-remove-yaml
