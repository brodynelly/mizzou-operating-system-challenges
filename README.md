# Mizzou Operating System Challenges

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![CI](https://github.com/brodynelly/mizzou-operating-system-challenges/actions/workflows/ci.yml/badge.svg)](https://github.com/brodynelly/mizzou-operating-system-challenges/actions/workflows/ci.yml) ![C](https://img.shields.io/badge/C-C11-blue?logo=c)

C implementations of operating-systems coursework: C fundamentals, process scheduling, threading, block storage, and a Unix-style filesystem. The assignment directories retain their original course layouts.

## Assignments

| Assignment | Topic | Directory |
| --- | --- | --- |
| A2 | C fundamentals: arrays, strings, allocation, and bit operations | `a2_c_refresher_bsn3g9-master/` |
| A3 | Process scheduling simulator | `a3_process_scheduling.sp2025_bsn3g9-main/` |
| A3.5 | POSIX threading | `a3.5-threading_bsn3g9-main/` |
| A4 | Block storage | `a4_block_store_bsn3g9-master/` |
| A5 | Inode-based filesystem | `a5_fs2021_bsn3g9-master/` |

## Build prerequisites

The projects use CMake, GCC or Clang, and GoogleTest for C++ test harnesses. Required compiler versions and libraries vary by assignment. Several original CMake files refer to course-cluster include and library directories, so a local build may need environment-specific setup.

For example, the A4 CMake project can be configured and built with:

```sh
cd a4_block_store_bsn3g9-master
cmake -S . -B build
cmake --build build --target assignment4_test
```

When the assignment's GoogleTest dependency is available, run its generated test executable from the build directory. Target and executable names differ across assignments; see each directory's `CMakeLists.txt` and [test notes](tests/README.md).

## Verification

GitHub Actions checks active C translation units with GCC in C11 syntax-only mode. The A5 CMake project builds src/FS.c; its earlier FS_M1.c and FS_M2.c milestone implementations are not part of that target and are excluded from this gate. A compiler error in an active source file fails the job. This check does not link binaries, compile C++ test harnesses, or run the assignment GoogleTest suites.

## Project structure

```text
.
|-- a2_c_refresher_bsn3g9-master/       # C fundamentals
|-- a3_process_scheduling.sp2025_bsn3g9-main/ # Scheduler simulator
|-- a3.5-threading_bsn3g9-main/         # POSIX threads
|-- a4_block_store_bsn3g9-master/       # Block store
|-- a5_fs2021_bsn3g9-master/            # Filesystem
`-- tests/                              # Repository-level test notes
```

## License

MIT. See [LICENSE](LICENSE).
