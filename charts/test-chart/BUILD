load("@bazel_tools//tools/build_defs/pkg:pkg.bzl", "pkg_tar")

package(default_visibility = ["//visibility:public"])

filegroup(
    name = "allfiles",
    srcs = glob([
        "**",
    ]),
)

pkg_tar(
    name = "chart",
    srcs = glob(["**"]),
    extension = "tar.gz",
    #package_dir = ".",
    strip_prefix = ".",
)
