load("@io_bazel_rules_docker//python:image.bzl", "py_image")
load("@io_bazel_rules_docker//docker:docker.bzl", "docker_build")

py_image(
    name = "hello_py",
    srcs = ["hello.py"],
    base = "gcr.io/distroless/python2.7",
    main = "hello.py",
    layers = [
        #requirement("flask")
    ]
)

docker_build(
    name = "hello",
    base = ":hello_py",
)
