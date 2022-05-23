To install the patch operator https://github.com/redhat-cop/patch-operator#patch-operator 

Apply the following manifests:

# Create namespace
oc apply -f namespace.yaml

# Create subscription / deploy operator
oc apply -f subscription.yaml

Next, it is important to create a service account with the correct cluster rolebinding so the patch operator can have the authorization to apply the neccessary patches. 
Here, we crate a patch-superuser service account with cluster-admin permissions. This is done by:

# Create the service account
oc apply -f service-account.yaml

# Create the correct cluster rolebinding
oc apply -f cluster-rolebinding.yaml
