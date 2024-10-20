load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Change master to the git tag you want.
http_archive(
    name = "rules_r",
    strip_prefix = "rules_r-master",
    urls = ["https://github.com/grailbio/rules_r/archive/master.tar.gz"],
)

load("@rules_r//R:dependencies.bzl", "r_register_toolchains", "r_rules_dependencies")

r_rules_dependencies()
# TODO(@waflores) need to sort out how to invoke a bazel provided R binary
r_register_toolchains()