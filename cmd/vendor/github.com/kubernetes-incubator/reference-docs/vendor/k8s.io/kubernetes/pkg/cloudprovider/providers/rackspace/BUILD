package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["rackspace.go"],
    importpath = "k8s.io/kubernetes/pkg/cloudprovider/providers/rackspace",
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/rackspace/gophercloud:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/openstack/compute/v2/extensions/volumeattach:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/openstack/compute/v2/servers:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/pagination:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/rackspace:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/rackspace/blockstorage/v1/volumes:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/rackspace/compute/v2/servers:go_default_library",
        "//vendor/github.com/rackspace/gophercloud/rackspace/compute/v2/volumeattach:go_default_library",
        "//vendor/gopkg.in/gcfg.v1:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/cloudprovider:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/controller:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["rackspace_test.go"],
    importpath = "k8s.io/kubernetes/pkg/cloudprovider/providers/rackspace",
    library = ":go_default_library",
    deps = ["//vendor/github.com/rackspace/gophercloud:go_default_library"],
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
