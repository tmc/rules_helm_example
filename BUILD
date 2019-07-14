load("@com_github_tmc_rules_helm//helm:helm.bzl", "helm_release")

# Basic example that shows creating a release.
helm_release(
    name = "test_chart_1",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-1",
    values_yaml = "//:test_chart_values.yaml",
)

# Example showing the same chart and values as before creating a separate release.
helm_release(
    name = "test_chart_2",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-2",
    values_yaml = "//:test_chart_values.yaml",
)

# Example showing passing values directly without using a values.yaml file.
helm_release(
    name = "test_chart_3",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-3",
    values = {
        "replicaCount": 2,
    }
)

# Example showing a chart with dependencies.
helm_release(
    name = "test_chart_with_deps",
    chart = "//charts/test-chart-with-deps:chart",
    release_name = "test-release-3",
    values_yaml = "//:test_chart_values.yaml",
)

sh_test(
    name = "dummy_test",
    srcs = ["dummy_test.sh"],
)
