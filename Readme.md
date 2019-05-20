# load-gen

A simple load generator for kubernetes using helm.

There are times when you just want to generate some background load to stress-test your software on a cluster. This is especially
useful when you're looking to test the scale out and in properties of your cluster as you deploy and load-test applications.

This chart is really quite simple. It uses a short ruby script in a configmap that gets mounted and run on a ruby-alpine image.
The current defaults will generate a 1500-2000 milli-cpu load on a DS3_v2 Azure instance.

It runs as a daemonset so each node in the cluster will have computation run on it.


**To Install**

- Run:

    > helm install load-gen --name load-gen

