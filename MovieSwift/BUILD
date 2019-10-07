load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

swift_library(
    name = "MovieSwiftLib",
    srcs = glob(["MovieSwift/**/*.swift"]),
    deps = ["@SwiftUIFlux"],
)

ios_application(
    name = "MovieSwift",
    bundle_id = "sh.aky.Sandbox",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["MovieSwift/Info.plist"],
    minimum_os_version = "13.0",
    deps = ["MovieSwiftLib"],
)
