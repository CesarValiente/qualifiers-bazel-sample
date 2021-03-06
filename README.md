# qualifiers-bazel-sample

This is a sample app that shows how resource qualifiers are used on Surface Duo devices.
The sample purpose is also to be a as a playground to experiment with [Bazel](https://bazel.build/start) to build and deploy the app.

## How to build and deploy?

1. In the terminal, go inside the project's folder (e.g. /foo/bar/qualifiers-bazel-sample).
2. To build the app, type in the terminal `bazel build //src/main:app`.
3. To deploy/install the app in your device/emulator, type `bazel mobile-install //src/main:app`.

If you need to clean the project after a previous build, type `bazel clean`.

## How resource qualifiers work on Surface Duo?

The app will show different `layouts` and `strings` depending on the device/emulator you are using and how the app is displayed (single screen mode or spanned).

![Surface Duo 1 - single screen mode](art/surface-duo1-single-screen-mode.png)
![Surface Duo 1 - spanned mode](art/surface-duo1-spanned-mode.png)

![Surface Duo 2 - single screen mode](art/surface-duo2-single-screen-mode.png)
![Surface Duo 2 - spanned mode](art/surface-duo2-spanned-mode.png)

## Resources

### Qualifiers and Surface Duo
- [Providing resources](https://developer.android.com/guide/topics/resources/providing-resources).
- [Surface Duo dimensions](https://docs.microsoft.com/dual-screen/android/surface-duo-dimensions).
- [Surface Duo resource qualifiers](https://docs.microsoft.com/dual-screen/android/platform/resource-qualifier).
- [Surface Duo emulator](https://docs.microsoft.com/dual-screen/android/emulator/surface-duo-download). Download it now! :-)

### Bazel essential docs
- [Bazel](https://bazel.build/).
- [Installing Bazel in your computer](https://bazel.build/install).
- [Bazel Build encyclopedia](https://bazel.build/reference/be/overview).  
- [Android rules Bazel docs](https://bazel.build/reference/be/android).  

### Building an Android app
- [Build an Android app (Java)](https://bazel.build/tutorials/android-app).
- [Build an Android app (Kotlin)](https://github.com/bazelbuild/rules_jvm_external/tree/master/examples/android_kotlin_app).
- [Build an Android app (Kotlin) another example](https://github.com/scalio/Android-Bazel-Starter-Kotlin).  

### Rules and releases
- [Kotlin releases](https://github.com/JetBrains/kotlin/releases) to update `rules_kotlin_compiler_release` in the `workspace`.
- [Rules JVM external](https://github.com/bazelbuild/rules_jvm_external/releases) to update `rules_jvm_external` in the `workspace`.
- [Rules Kotlin](https://github.com/bazelbuild/rules_kotlin/releases) to update the `rules_kotlin` in the `workspace`.
- [Rules Android](https://github.com/bazelbuild/rules_android). Abandoned? Not needed to build our sample.

### IntelliJ/Android Studio Bazel plugin
- [IntelliJ/Android Studio Bazel plugin](https://ij.bazel.build/docs/bazel-plugin.html).


## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## License

Copyright (c) Microsoft Corporation.

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Other copyrights

Images located  in `/res` folder are taken from **Microsoft Paint 3D**. You can download and install the app from the [Microsoft Store](https://www.microsoft.com/en-us/p/paint-3d/9nblggh5fv99).