workspace(name="com_github_tmc_rules_helm_example")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository", "new_git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

git_repository(
    name = "com_github_tmc_rules_helm",
    branch = "master",
    remote = "https://github.com/tmc/rules_helm.git",
)
# local_repository(name = "com_github_tmc_rules_helm", path = "../rules_helm")

load("@com_github_tmc_rules_helm//:repos.bzl", "helm_repositories")

helm_repositories()

# Istio example
ISTIO_REF = "9b6d31b74d1c0cc9358cc82d395b53f71393326b"  # 1.1.5

ISTIO_SHA256 = "0f672d780a34f379d5a83b3b0317b370e1bf7e09f07a1486c6536ae124e2db5d"

http_archive(
    name = "com_github_istio_istio",
    build_file = "@//charts/istio:BUILD.istio",
    sha256 = ISTIO_SHA256,
    strip_prefix = "istio-%s" % ISTIO_REF,
    url = "https://github.com/istio/istio/archive/%s.zip" % ISTIO_REF,
)
