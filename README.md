# qualifiers-bazel-sample

This is a sample app that shows how resource qualifiers are used on Surface Duo devices.
The sample purpose is also to be a as a playground to experiment with [Bazel](https://bazel.build/start) to build and deploy the app.

## Resources

### Learning
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
