package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["webhook.go"],
    tags = ["automanaged"],
    deps = [
        "//pkg/apis/authorization/install:go_default_library",
        "//pkg/apis/authorization/v1beta1:go_default_library",
        "//pkg/auth/authorizer:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/authorization/v1beta1:go_default_library",
        "//pkg/runtime/schema:go_default_library",
        "//pkg/util/cache:go_default_library",
        "//plugin/pkg/webhook:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "certs_test.go",
        "webhook_test.go",
    ],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/apis/authorization/v1beta1:go_default_library",
        "//pkg/apis/meta/v1:go_default_library",
        "//pkg/auth/authorizer:go_default_library",
        "//pkg/auth/user:go_default_library",
        "//pkg/client/unversioned/clientcmd/api/v1:go_default_library",
        "//pkg/util/diff:go_default_library",
    ],
)
