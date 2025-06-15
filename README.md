# Helm Chart Quality Gate

According to development process i have been issued with problems of helm-chart compatibility with my applications, API-versions, helm-hooks testing and cronjobs debugging.
I decided to create an example project with some Quality Gates of my own.

## Stages of Quality Gate

`Linting` - basic helm lint of YAML structure
`Schema compatibility check` - because of Kubernetes API and CRDs changes
`Unit test` - some helm unit tests
`Dry-run` - deploing our application to [kind](https://kind.sigs.k8s.io/) cluster

## Tools

`Taskfile` - task runner, alternative to Makefile
`Kind` - kubernetes in docker cluster
`Helm` - kubernetes application package manager
`Chart-testing` - tool for lintin and testing helm-chart pull requests
`Helm-unittest` - tool for unit testing helm templates
`Kubeconform` - kubernetes manifest validation tool
