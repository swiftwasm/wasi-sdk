# WASI SDK

[![Build Status](https://dev.azure.com/swiftwasm/wasi-sdk/_apis/build/status/swiftwasm.wasi-sdk?branchName=swiftwasm)](https://dev.azure.com/swiftwasm/wasi-sdk/_build/latest?definitionId=1&branchName=swiftwasm)

## Quick Start

[Download SDK packages here.](https://github.com/CraneStation/wasi-sdk/releases)

## About this repository

This repository contains no compiler or library code itself; it uses
git submodules to pull in the upstream Clang and LLVM tree, as well as the
wasi-sysroot tree.

The Sysroot portion of this SDK is the
[wasi-sysroot](https://github.com/CraneStation/wasi-sysroot).

Upstream Clang and LLVM 8.0 can compile for WASI out of the box, and WebAssembly
support is included in them by default. So, all that's done here is to provide
builds configured to set the default target and sysroot for convenience.

One could also use a standard Clang 8.0, build a sysroot from the sources
mentioned above, and compile with
"--target=wasm32-unknown-wasi --sysroot=/path/to/sysroot".
