# Example Project For CMake LLVM IR Pipelines

## Introduction

This repo provides an example usage for [LLVM IR cmake pipelines][1].

## Requirements

-   [cmake][1] 3.2.0 or later
-   [LLVM IR cmake pipelines][2]
-   [LLVM IR cmake utilities][3]
-   [LLVM/Clang][4]

## How To Use

1.  `git clone --recursive` this repo.
2.  Create a directory for an out-of-source build and `cd` into it.
3.  Provide the appropriate option to `cmake` during configuration.
    For examples on the various options have a look at the export scripts (provided for convenience) located in the
    `utils/scripts/build` subdirectory. Then, you can use the `build.sh` script located in the same directory to build
    the project.

## Quick Overview

This repository provides 2 example uses for generating `LLVM` IR bitcode using:

-   [LLVM IR cmake pipelines][2]
-   [LLVM IR cmake utilities][3]

First, the subproject under the subdirectory `statically` shows how to use a chain/pipeline of various `LLVM` `opt`
passes by specifying them in the lists file. For this, see the configuration options in the following export scripts 
under `utils/scripts/build`:

-   `exports_deps1.sh`
-   `exports_deps2.sh`

Second, the subproject under the subdirectory `dynamically` provides a working example on how to chain/pipeline and
group passes by specifying their order during configuration. For this, see the configuration options in the following
export scripts under `utils/scripts/build`:

-   `exports_deps3.sh`
-   `exports_deps4.sh`

[1]: https://github.com/compor/llvm-ir-cmake-pipelines

[2]: https://github.com/compor/llvm-ir-cmake-pipelines

[3]: https://github.com/compor/llvm-ir-cmake-utils

[4]: https://llvm.org
