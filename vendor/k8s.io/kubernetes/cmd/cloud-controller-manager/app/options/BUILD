package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["options.go"],
    importpath = "k8s.io/kubernetes/cmd/cloud-controller-manager/app/options",
    deps = [
        "//cmd/cloud-controller-manager/app/config:go_default_library",
        "//cmd/controller-manager/app/options:go_default_library",
        "//pkg/client/leaderelectionconfig:go_default_library",
        "//pkg/features:go_default_library",
        "//pkg/master/ports:go_default_library",
        "//vendor/github.com/spf13/pflag:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/util/feature:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)

go_test(
    name = "go_default_test",
    srcs = ["options_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//cmd/controller-manager/app/options:go_default_library",
        "//pkg/apis/componentconfig:go_default_library",
        "//vendor/github.com/spf13/pflag:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/diff:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/server/options:go_default_library",
    ],
)
