load("@notebooks//:requirements.bzl", "requirement")

py_binary(
    name = "jupyter",
    srcs = ["jupyter.py"],
    deps = [
        "//foo:bar",
        requirement("notebook"),
    ],
)
