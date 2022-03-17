
#----- Sets Android SDK and define the specific build tools we want to use -----#
android_sdk_repository(
    name = "androidsdk",
    build_tools_version = "30.0.3")

#---- Load rules and tools that will be used to build the project ----#
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

#---- JVM rules needed to use later artifact repositories and their JVM dependencies ---#
RULES_JVM_EXTERNAL_TAG = "4.2"
RULES_JVM_EXTERNAL_SHA = "cd1a77b7b02e8e008439ca76fd34f5b07aecb8c752961f9640dea15e9e5ba1ca"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

#---- Using JVM rules, we will be able to use artifact feeds such as Maven and Google with their dependencies ---#
load("@rules_jvm_external//:defs.bzl", "maven_install")

#--- We download and load the dependecies we want to use. Currently we just define Google's Maven repo.
# Maven Central ( "https://repo1.maven.org/maven2" )  should be added in the `repositories` node as well when needed. ----#
maven_install(
    artifacts = [
        "androidx.appcompat:appcompat:1.0.2",
        "com.google.android.material:material:1.0.0",
    ],
    repositories = [
        "https://maven.google.com",
    ],
    fetch_sources = True,
)

#---- Here we define the `rules_kotlin_version` we are going to use, needed to build Kotlin based projects ----#

#Having issues with the latest version
# rules_kotlin_version = "v1.5"
# rules_kotlin_sha = "12d22a3d9cbcf00f2e2d8f0683ba87d3823cb8c7f6837568dd7e48846e023307"

rules_kotlin_version = "legacy-1.4.0-rc4"
rules_kotlin_sha = "9cc0e4031bcb7e8508fd9569a81e7042bbf380604a0157f796d06d511cff2769"
http_archive(
    name = "io_bazel_rules_kotlin",
    sha256 = rules_kotlin_sha,
    urls = ["https://github.com/bazelbuild/rules_kotlin/releases/download/%s/rules_kotlin_release.tgz" % rules_kotlin_version],
)

#---- We define here the Kotlin compiler version we use. We can skip this and then not define the `compiler_release` we use
# when we load the `kotlin_repositories` right after this ---- #
kotlin_version = "1.6.20-RC"
kotlin_release_sha = "2f78ced6b983db49ea1cbcbe41c18bff19ced596861f6bd8af01311d71b6d81d"
rules_kotlin_compiler_release = {
    "urls": [
    "https://github.com/JetBrains/kotlin/releases/download/v{v}/kotlin-compiler-{v}.zip".format(v = kotlin_version),
    ],
    "sha256": kotlin_release_sha,
}

#--- Load the `kotlin_repositories` we will use ----#
load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kotlin_repositories")
kotlin_repositories(compiler_release = rules_kotlin_compiler_release)


#--- Load the toolchains we will use ---- #
load("@io_bazel_rules_kotlin//kotlin:kotlin.bzl", "kt_register_toolchains")
kt_register_toolchains()