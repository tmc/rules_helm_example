# rules_helm_example

This repository shows example use of the [rules_helm](https://github.com/tmc/rules_helm) Bazel build
rules.

Examples:
* `bazel run //:test_chart_1.install` this will install the chart defined in BUILD to the currently configured kubernetes cluster.
* `bazel run //charts/istio:istio_init.install` and `bazel run //charts/istio:istio.install` will install Istio.
