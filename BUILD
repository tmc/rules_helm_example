genrule(
    name = "gr_tarball",
    srcs = ["//charts/test-chart:tarball"],
    outs = ["letarball.tar.gz"],
    cmd = "cp ./$(location //charts/test-chart:tarball) $@",
)

sh_binary(
    name = "ls_tar",
    srcs = ["ls_tar.sh"],
    data = [
        ":gr_tarball",
        "//charts/test-chart:tarball",
    ],
    args = [
        "$(location //charts/test-chart:tarball)",
        "$(location :gr_tarball)",
    ],
    deps = ["@bazel_tools//tools/bash/runfiles"],
)
