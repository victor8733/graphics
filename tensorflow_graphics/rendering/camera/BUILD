#Copyright 2018 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# Camera functionalities for tf-graphics.

# google internal)

licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

py_library(
    name = "perspective",
    srcs = ["perspective.py"],
    srcs_version = "PY2AND3",
    deps = [
        # google internal,
        "//tensorflow_graphics/util:export_api",
        "//tensorflow_graphics/util:safe_ops",
        "//tensorflow_graphics/util:shape",
    ],
)

py_library(
    name = "orthographic",
    srcs = ["orthographic.py"],
    srcs_version = "PY2AND3",
    deps = [
        # google internal,
        "//tensorflow_graphics/util:export_api",
        "//tensorflow_graphics/util:shape",
    ],
)

py_library(
    name = "quadratic_radial_distortion",
    srcs = ["quadratic_radial_distortion.py"],
    srcs_version = "PY2AND3",
    deps = [
        # google internal,
        "//tensorflow_graphics/util:asserts",
        "//tensorflow_graphics/util:export_api",
        "//tensorflow_graphics/util:shape",
    ],
)

py_library(
    name = "camera",
    srcs = ["__init__.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":orthographic",
        ":perspective",
        ":quadratic_radial_distortion",
        "//tensorflow_graphics/util:export_api",
    ],
)

py_test(
    name = "perspective_test",
    srcs = ["tests/perspective_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":perspective",
        # package dep

        # google internal,
        "//tensorflow_graphics/util:test_case",
    ],
)

py_test(
    name = "orthographic_test",
    srcs = ["tests/orthographic_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":orthographic",
        # package dep

        # google internal,
        "//tensorflow_graphics/util:test_case",
    ],
)

py_test(
    name = "quadratic_radial_distortion_test",
    srcs = ["tests/quadratic_radial_distortion_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":quadratic_radial_distortion",
        # package dep

        # google internal,
        "//tensorflow_graphics/util:test_case",
    ],
)
