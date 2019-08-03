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
ISTIO_REF="cd4a148f37dc386986d6a6d899778849e686beea" # 1.2.2
ISTIO_SHA256="a30b152094f0c80887de7f342e3549903e8852a2a6949e2d3e99cf447c5e1afb"
http_archive(
    name = "com_github_istio_istio",
    build_file = "@//charts/istio:BUILD.istio",
    sha256 = ISTIO_SHA256,
    strip_prefix = "istio-%s" % ISTIO_REF,
    url = "https://github.com/istio/istio/archive/%s.zip" % ISTIO_REF,
)
