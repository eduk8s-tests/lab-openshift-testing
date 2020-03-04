LAB - OpenShift Sample
======================

Sample workshop content which also embeds the OpenShift web console.

This is a copy of ``lab-markdown-sample``, but with additional configuration
to start up an embedded OpenShift web console. The configuration required to
do this is found in the following files:

* ``resources/workshop.yaml``
* ``workshop/gateway.yaml``

You should preserve the relevant parts of those files when adapting this to
your own OpenShift specific workshop.

Note that if you attempt to run the OpenShift web console on a plain
Kubernetes cluster, many features of the web console will not work.

If wishing to disable the Kubernetes dashboard, then uncomment the setting
of:

```
ENABLE_CONSOLE=false
```

in the ``Dockerfile`` if building a workshop image.

Alternatively, uncomment the similar setting in ``resources/workshop.yaml``.
The latter will be required if you are going to use the feature of
downloading workshop content from a GitHub repository when using the
standard workshop dashboard base image, rather than build a custom workshop
image.
