# C++ startup
A minimal C++20 starter project with a ready-to-use build and debugging setup for macOS and Windows.

## Features
- Minimal C++20 starter project for macOS and Windows with a runnable `Hello, World!` example.
- Clang builds with CMake and Ninja Multi-Config presets for Debug, Release, and RelWithDebInfo.
- VS Code build and debug tasks with CodeLLDB launch configurations.
- Compilation database generation, clangd diagnostics with clang-tidy checks, and clang-format settings.

## Prerequisites
The project targets macOS and Windows. The build environment requires the following dependencies:
- CMake
- Ninja
- Xcode on macOS or LLVM with Visual Studio on Windows

These dependencies can be installed manually or through package managers.

On macOS [Homebrew](https://brew.sh/) can install some prerequisites using the following command. Install Xcode separately.
```shell
brew install cmake ninja
```

On Windows [Scoop](https://scoop.sh/) can install some prerequisites using the following command. Install Visual Studio separately.
```shell
scoop install cmake ninja llvm
```

## Quick start
```shell
git clone --recurse-submodules https://github.com/liamhauw/cpp_startup.git
cd cpp_startup
cmake --preset=Base
cmake --build --preset=Release
cmake --install build --config Release
./bin/cpp_startup_engine
```

## Contributions
### Update submodule
```shell
git pull --recurse-submodules
git submodule update --remote
```

### Debug
Install VSCode with clangd and CodeLLDB extensions.
Click Run and Debug in the sidebar, and select Debug or RelWithDebInfo. Click Start Debugging or press F5.