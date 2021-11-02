# googletest-ci

| **CI Service** | Build Status |
|:---------------|-------------:|
| GitHub Actions | [![Build Status (GitHub Actions)](https://github.com/GHF/googletest-ci/workflows/CMake%20Tests/badge.svg)](https://github.com/GHF/googletest-ci/actions?query=workflow%3A"CMake%20Tests") |
| CircleCI | [![Build Status (CircleCI)](https://circleci.com/gh/GHF/googletest-ci.svg?style=svg)](https://circleci.com/gh/GHF/googletest-ci) |
| Azure Pipelines | [![Build Status](https://dev.azure.com/xow/github-googletest-ci/_apis/build/status/GHF.googletest-ci)](https://dev.azure.com/xow/github-googletest-ci/_build/latest?definitionId=1) |

Example of unit testing with [Google Test](https://code.google.com/p/googletest)
compiled with CMake and deployed to various continuous integration (CI) systems.

Dependency management is performed by CMake's
[FetchContent](https://cmake.org/cmake/help/latest/module/FetchContent.html)
module, a part of CMake as of version 3.11 that works much like Google Test's
[ExternalProject method](https://github.com/google/googletest/blob/v1.8.x/googletest/README.md#incorporating-into-an-existing-cmake-project).
This can fetch and build Google Test at a specific revision in a more concise
way than scripting CI to download, extract, and build release packages, all
while making it easier for somebody who downloads this project to run the tests
with minimal steps.

## Manual build & run

After cloning, to build:

```
cmake -S . -B mybuild
cd mybuild
cmake --build .
```

Then to run:

```
ctest
```

## License

Public domain-like, under [CC0](https://creativecommons.org/publicdomain/zero/1.0/). [![License CC0](https://img.shields.io/badge/license-CC0-blue.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
