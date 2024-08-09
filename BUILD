load("@build_bazel_rules_apple//apple:apple.bzl", "apple_dynamic_xcframework_import")
load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

ios_application(
    name = "MyApp",
    bundle_id = "com.vakhid.my-app",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info.plist"],
    minimum_os_version = "14.0",
    deps = [
        ":PhoneNumberKit",
        ":swift_main_lib",
    ],
)

swift_library(
    name = "swift_main_lib",
    srcs = ["main.swift"],
)

apple_dynamic_xcframework_import(
    name = "PhoneNumberKit",
    xcframework_imports = glob(["PhoneNumberKit.xcframework/**"]),
)