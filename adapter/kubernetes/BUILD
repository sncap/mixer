package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "cache.go",
        "kubernetes.go",
    ],
    deps = [
        "//adapter/kubernetes/config:go_default_library",
        "//pkg/adapter:go_default_library",
        "@io_k8s_client_go//kubernetes:go_default_library",
        "@io_k8s_client_go//pkg/api:go_default_library",
        "@io_k8s_client_go//pkg/api/v1:go_default_library",
        "@io_k8s_client_go//pkg/runtime:go_default_library",
        "@io_k8s_client_go//pkg/watch:go_default_library",
        "@io_k8s_client_go//rest:go_default_library",
        "@io_k8s_client_go//tools/cache:go_default_library",
        "@io_k8s_client_go//tools/clientcmd:go_default_library",
    ],
)

go_test(
    name = "small_tests",
    size = "small",
    srcs = [
        "cache_test.go",
        "kubernetes_test.go",
    ],
    library = ":go_default_library",
    deps = ["//pkg/adapter/test:go_default_library"],
)
