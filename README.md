# Kubernetes Label Operator

This operator adds a `ball.pk/pod-name` label to Pods with the
`ball.pk/add-pod-name-label=true` annotation. The label's value is the Pod's
name.

This is created by following the tutorial from https://kubernetes.io/blog/2021/06/21/writing-a-controller-for-pod-labels/

## Usage

To run the operator locally on your Kubernetes cluster:

```bash
make run
```

To build and release a Docker image for the operator:

```bash
make IMG=docker.io/busser/label-operator docker-build docker-push
```

To deploy the operator to your Kubernetes cluster:

```bash
make IMG=docker.io/busser/label-operator deploy
```

## Testing

To run unit tests:

```bash
make test
```