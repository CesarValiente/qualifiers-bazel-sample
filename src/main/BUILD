#--- We load the specific rules we want to use here:
# - artifact (JVM) to get dependencies from an artifact feed.
# - kotlin_android_library to build a kotlin android project.

load("@rules_jvm_external//:defs.bzl", "artifact")
load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kt_android_library")

PACKAGE = "com.cesarvaliente.qualifiers"
MANIFEST = "AndroidManifest.xml"

#--- Used to build the Android resources ---#
android_library(
    name = "lib_res",
    custom_package = PACKAGE,
    manifest = MANIFEST,
    resource_files = glob(["res/**"]),
    enable_data_binding = False,
     deps = [
            artifact("com.google.android.material:material"),
        ],
)

#--- Used to build the Kotlin resources on top of the Android ones. ---#
kt_android_library(
    name = "lib_kt",
    srcs = glob(["java/**/*.kt"]),
    deps = [
        ":lib_res",
        artifact("androidx.appcompat:appcompat"),
    ]
)

#--- We then make the binary with the resources we previously have built ----#
android_binary(
    name = "app",
    manifest = MANIFEST,
    custom_package = PACKAGE,
    manifest_values = {
        "minSdkVersion": "21",
        "versionCode" : "1",
        "versionName" : "1",
        "targetSdkVersion": "29",
    },
    deps = [
        ":lib_res",
        ":lib_kt",
    ],
)