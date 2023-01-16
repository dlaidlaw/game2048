# Example Code Deployments

These examples may be used to test the cluster, or as a working example
of how to write your own deployments.

# 2048

This is a game where you try to join the numbers in a grid to make them add up
to 2048.

This example demonstrates how to use the aws-load-balancer-controller to create
an AWS ALB. The ALB is fully configured with SSL, and uses IP targeting mode 
which will also work for Fargate pods.

If you would like to have the controller automatically add a readiness gate to
the pods targeted by the ALB, you must add a label to the namespace being used:
* elbv2.k8s.aws/pod-readiness-gate-inject=enabled

The readiness gate injector will ignore any pods in any namespace that does not
have that annotation.

Examine the annotations on the Ingress object, you may need to change these for
your cluster/account/DNS setup.

If you would like to deploy via helm, please check out the helm in other examples to practice. Also, be sure to always check out AWS and Helm documentation!
