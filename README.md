# googletest-ci

| **CI Service** | Build Status |
|:---------------|-------------:|
| CircleCI | [![Build Status (CircleCI)](https://circleci.com/gh/GHF/googletest-ci.svg?style=svg)](https://circleci.com/gh/GHF/googletest-ci) |
| Shippable | [![Build Status (Shippable)](https://api.shippable.com/projects/58cd9b7935d7240600ba0471/badge?branch=master)](https://app.shippable.com/github/GHF/googletest-ci) |
| Travis | [![Build Status (Travis)](https://travis-ci.org/GHF/googletest-ci.svg?branch=master)](https://travis-ci.org/GHF/googletest-ci) |

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
mkdir mybuild
cd mybuild
cmake ..
make
```

Then to run:

```
./foo_test
```

## License

Public domain-like, under [CC0](https://creativecommons.org/publicdomain/zero/1.0/). [![License CC0](https://img.shields.io/badge/license-CC0-blue.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
