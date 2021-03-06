# Description:
#   Contains the Slim library, including common neural networks and examples.

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

package(default_visibility = ["//tensorflow:__subpackages__"])

py_library(
    name = "evaluation",
    srcs = ["python/slim/evaluation.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow/python:framework",
        "//tensorflow/python:ops",
        "//tensorflow/python:platform",
        "//tensorflow/python:training",
    ],
)

py_test(
    name = "evaluation_test",
    srcs = ["python/slim/evaluation_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow:tensorflow_py",
        "//tensorflow/contrib/slim",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_library(
    name = "learning",
    srcs = ["python/slim/learning.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow/python:framework",
        "//tensorflow/python:ops",
        "//tensorflow/python:platform",
        "//tensorflow/python:training",
    ],
)

py_test(
    name = "learning_test",
    srcs = ["python/slim/learning_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow:tensorflow_py",
        "//tensorflow/contrib/slim",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_library(
    name = "queues",
    srcs = ["python/slim/queues.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow/python:ops",
        "//tensorflow/python:training",
    ],
)

py_library(
    name = "slim",
    srcs = [
        "__init__.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        ":evaluation",
        ":learning",
        ":queues",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
