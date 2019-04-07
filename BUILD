load("@com_github_tmc_rules_helm//:helm.bzl", "helm_chart_installer")

filegroup(
    name = "allfiles",
    srcs = glob([
        "**/*",
    ]),
)

helm_chart_installer(
    name = "test_chart",
    chart = "//charts/test-chart:chart",
    release_name = "test-release-1",
    values_yaml = "//:test_chart_values.yaml",
)
