load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")
load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:prefix github.com/henrywong-seekers/bazel-test
gazelle(name = "gazelle")

go_library(
    name = "go_default_library",
    srcs = ["hello.go"],
    importpath = "github.com/henrywong-seekers/bazel-test",
    visibility = ["//visibility:private"],
    deps = ["//cmd:go_default_library"],
)

go_binary(
    name = "bazel-test",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)
