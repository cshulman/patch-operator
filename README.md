This repo contains manifests for installing the patch-operator on an OpenShift cluster. More information about the patch-operator can be found https://github.com/redhat-cop/patch-operator#deploying-the-operator


- To utilize, first install the patch-operator by applying the manifests in the 'install' directory

- Next, apply any/all of the patches located in the 'patches' directory

- The 'manual' directory contains manifests that can be applied manually to accomplish the same results as the manifests in the 'patches' directory, but without the patch-operator to manage them.
