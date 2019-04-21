load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository", "new_git_repository")

git_repository(
    name = "com_github_tmc_rules_helm",
    branch = "master",
    remote = "https://github.com/tmc/rules_helm.git",
)
# local_repository(name = "com_github_tmc_rules_helm", path = "../rules_helm")

load("@com_github_tmc_rules_helm//:repos.bzl", "helm_repositories")

helm_repositories()
