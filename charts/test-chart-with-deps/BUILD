load("@com_github_tmc_rules_helm//:helm.bzl", "helm_chart")

package(default_visibility = ["//visibility:public"])

helm_chart(
    name = "chart",
    update_deps = True,
    srcs = glob(["**"]),
)
