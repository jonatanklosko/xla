load("//xla/stream_executor:build_defs.bzl", "if_cuda_or_rocm",)
load("@local_config_cuda//cuda:build_defs.bzl", "if_cuda",)
load("@local_config_rocm//rocm:build_defs.bzl", "if_rocm",)
load("//xla/tsl:tsl.bzl", "if_with_tpu_support")
load("//xla/tsl:tsl.bzl", "tsl_grpc_cc_dependencies",)
load("//xla/tsl:tsl.bzl", "transitive_hdrs",)
load("@rules_pkg//pkg:tar.bzl", "pkg_tar")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_file")

package(default_visibility=["//visibility:private"])


# See https://github.com/bazelbuild/rules_pkg/issues/517#issuecomment-1492917994
genrule(
  name = "xla_extension",
  outs = ["xla_extension.tar.gz"],
  srcs = [
  ],
  cmd = """
    mkdir xla_extension
    touch xla_extension/test.txt
    # Create the final package tarball
    tar czf "$@" xla_extension
  """
)
