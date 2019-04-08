sh_binary(
    name = "ls_tar",
    srcs = ["ls_tar.sh"],
    data = ["//charts/test-chart:tarball"],
    deps = ["@bazel_tools//tools/bash/runfiles"],
    args = ["$(location //charts/test-chart:tarball)"],
)
