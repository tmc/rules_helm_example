load("@com_github_tmc_rules_helm//helm:helm.bzl", "helm_release")

helm_release(
    name = "test_chart_1",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-1",
    values_yaml = "//:test_chart_values.yaml",
)

helm_release(
    name = "test_chart_2",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-2",
    values_yaml = "//:test_chart_values.yaml",
)

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
