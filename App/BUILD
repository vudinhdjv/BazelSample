load("//config:custom_rules.bzl", "application")
load(
    "@rules_xcodeproj//xcodeproj:defs.bzl",
    "top_level_target",
    "xcodeproj",
)
licenses(["notice"])

application(
    name = "Sample",
    infoplist = "Supporting Files/Info.plist",
    app_icons = [
        "//App/Resources:AppIcon",
    ],
    resources = [
        "//App/Resources:Assets",
    ],
    deps = [
        "//Modules/SwiftLibWithResources:SwiftLibWithResources",
        "//Modules/SwiftLib:SwiftLib",
        "//Carthage:Nimble",
    ]
)

xcodeproj(
    name = "xcodeproj",
    build_mode = "bazel",
    project_name = "Sample",
    tags = ["manual"],
    top_level_targets = [
        ":Sample",
    ],
)
