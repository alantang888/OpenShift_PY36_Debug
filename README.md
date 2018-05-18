# Python 3.6 environment for PyCharm remote debug on Minishift

The default root password is `changeme` you can modify it on deploy.yaml BuildConfig

Since we use root account for this container, then we need to let `useroot` service account can use `anyuid` on OpenShift
by run: 
```
oc adm policy add-scc-to-user anyuid -z useroot
```


reference:
https://docs.docker.com/engine/examples/running_ssh_service/