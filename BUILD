
genrule(
    name = "gr1",
    tools = ["//charts/test-chart:chart"],
    srcs = ["@com_github_tmc_rules_helm//:runfiles_bash"],
    outs = ["lstar.sh"],
    cmd = """
echo "#!/bin/bash" > $@
cp $(location @com_github_tmc_rules_helm//:runfiles_bash) $@
cat <<EOF >> $@
set -euo pipefail
echo $(location //charts/test-chart:chart)
#export RUNFILES_LIB_DEBUG=1

echo \$$1
echo \$$(rlocation $(location //charts/test-chart:chart))

ls -alh \$$1
ls -alh \$$(rlocation $(location //charts/test-chart:chart))
EOF""",
)

sh_binary(
    name = "ls_tar",
    srcs = ["lstar.sh"],
    deps = ["@bazel_tools//tools/bash/runfiles"],
    data = ["//charts/test-chart:chart", "@com_github_tmc_rules_helm//:helm"],
    args = ["$(location //charts/test-chart:chart)"],
)

#load("@com_github_tmc_rules_helm//:helm.bzl", "helm_chart_installer")
#
# helm_chart_installer(
#     name = "test_chartx",
#     chart = "//charts/test-chart:chart",
#     release_name = "test-release-1",
#     values_yaml = "//:test_chart_values.yaml",
# )

#genrule(
#    name = "test_chart",
#    srcs = ["@com_github_tmc_rules_helm//:runfiles_bash", "//:test_chart_values.yaml"],
#    tools = ["//charts/test-chart:chart"],
#    outs = ["runhelm.sh"],
#    #executable = 1,
#    #tools = ["@com_github_tmc_rules_helm//:helm"],
#    cmd = """
#cp $(location @com_github_tmc_rules_helm//:runfiles_bash) $@
#cat <<EOF >> $@
##export RUNFILES_LIB_DEBUG=1

#export HELM=\$$(rlocation com_github_tmc_rules_helm/helm)
#echo \$$HELM
#PATH=\$$PATH:\$$(dirname \$$HELM)
#echo CHARTLOCATION:
#export CHARTLOC=\$$(rlocation //charts/test-chart:chart")
##echo \$$1
##export CHARTLOC=./\$$1
#export CHARTLOC=$(location //charts/test-chart:chart")

#\$$HELM tiller run -- \$$HELM upgrade --install test-release-1 ./\$$CHARTLOC --values=$(location //:test_chart_values.yaml)
#EOF""",
#)

