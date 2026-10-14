# BSU-Qt: Modern C++ Desktop Engineering Curriculum

[![C++17](https://img.shields.io/badge/C%2B%2B-17-blue.svg)](https://en.wikipedia.org/wiki/C%2B%2B17)
[![Qt](https://img.shields.io/badge/Qt-GUI%20Framework-green.svg)](https://www.qt.io/)
[![Bazel](https://img.shields.io/badge/Bazel-Build%20System-43A047.svg)](https://bazel.build/)
[![Clang-Tidy](https://img.shields.io/badge/Clang--Tidy-Linted-00599C.svg)](https://clang.llvm.org/extra/clang-tidy/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An educational C++ and Qt engineering repository developed for the Advanced Qt Software Engineering curriculum at Belarusian State University, Faculty of Applied Mathematics and Computer Science. The project utilizes Bazel for modular dependency management and enforces code quality via Clang-Tidy and Clang-Format.

---

## Table of Contents
1. [Project Architecture](#project-architecture)
2. [Toolchain & Static Analysis](#toolchain--static-analysis)
3. [Prerequisites](#prerequisites)
4. [Build & Execution](#build--execution)
5. [Directory Structure](#directory-structure)
6. [License](#license)

---

## Project Architecture

The codebase enforces a layered modular structure:

* **Core Subsystem**: Headless C++ library encapsulating business logic, domain models, and data persistence without graphical dependencies.
* **Application Shell**: Qt GUI frontend implementing responsive viewports, custom widgets, action bars, and event handling.
* **Demos & Utilities**: Interactive showcase modules demonstrating Qt signals and slots, graphics rendering, and concurrency.

---

## Toolchain & Static Analysis

* **Bazel Modules**: Dependency graphs managed via `MODULE.bazel` and `BUILD.bazel`.
* **Clang-Tidy**: Enforces modernization rules, memory ownership conventions, and const-correctness.
* **Continuous Integration**: GitLab CI pipeline verifying clean builds, static analysis, and unit test success.

---

## Prerequisites

* Compiler: GCC 9+ or Clang 10+ with C++17 support
* Build System: Bazel 6.x or 7.x
* Qt Libraries: Qt development packages

```bash
sudo apt update
sudo apt install -y build-essential qtbase5-dev libqt5widgets5
```

---

## Build & Execution

Build and run using Bazel:

```bash
git clone git@github.com:botmaksim/qt.git
cd qt

bazel build //...
bazel test //...
bazel run //app:main
```

---

## Directory Structure

```text
qt/
├── MODULE.bazel             # Bazel module dependencies
├── BUILD.bazel              # Root build configuration
├── .clang-tidy              # Static analysis configuration
├── .clang-format            # Code formatting style rules
├── .gitlab-ci.yml           # Continuous integration pipeline
├── app/                     # Qt desktop application target
├── core/                    # Headless domain logic library
├── demos/                   # Interactive demonstration widgets
└── tools/                   # Build and lint helper scripts
```

---

## License

This project is open-source software licensed under the [MIT License](LICENSE).
