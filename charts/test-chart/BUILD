load("@bazel_tools//tools/build_defs/pkg:pkg.bzl", "pkg_tar")

package(default_visibility = ["//visibility:public"])

pkg_tar(
    name = "tarball",
    srcs = glob(["**"]),
    extension = "tar.gz",
    #package_dir = ".",
    strip_prefix = ".",
)
