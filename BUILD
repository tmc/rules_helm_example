load("@com_github_tmc_rules_helm//:helm.bzl", "helm_chart")

helm_chart(
    name = "test_chart_1",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-1",
    values_yaml = "//:test_chart_values.yaml",
)

helm_chart(
    name = "test_chart_2",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-2",
    values_yaml = "//:test_chart_values.yaml",
)

