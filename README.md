# Mizzou Operating System Challenges

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![CI](https://github.com/brodynelly/mizzou-operating-system-challenges/actions/workflows/ci.yml/badge.svg)](https://github.com/brodynelly/mizzou-operating-system-challenges/actions/workflows/ci.yml) ![C](https://img.shields.io/badge/C-C11-blue?logo=c)

C implementations of core OS concepts from University of Missouri's operating systems course — multithreading, process scheduling, block storage, and a Unix-style filesystem.

## Tech Stack

- **Language:** C (C11), C++ (test harnesses)
- **Build:** CMake
- **Testing:** GoogleTest (gtest)

## Assignments

| Assignment | Topic | Directory |
|---|---|---|
| A2 | C refresher — arrays, strings, allocation, bit manipulation | `a2_c_refresher_bsn3g9-master/` |
| A3 | Process scheduling simulator | `a3_process_scheduling.sp2025_bsn3g9-main/` |
| A3.5 | Multithreading | `a3.5-threading_bsn3g9-main/` |
| A4 | Block store implementation | `a4_block_store_bsn3g9-master/` |
| A5 | Unix-style filesystem (inode-based) | `a5_fs2021_bsn3g9-master/` |

## Getting Started

**Prerequisites:**
- GCC or Clang
- CMake ≥ 3.14
- GoogleTest (for running tests)

```bash
# Install deps (Arch / Ubuntu)
sudo pacman -S cmake gtest   # Arch
sudo apt install cmake libgtest-dev   # Ubuntu
```

**Build an assignment:**

```bash
cd a4_block_store_bsn3g9-master
mkdir build && cd build
cmake ..
make
```

## Usage

Each assignment is self-contained. Build with CMake, then run the test binary:

```bash
# Example: block store
cd a4_block_store_bsn3g9-master/build
./tests

# Example: process scheduling
cd a3_process_scheduling.sp2025_bsn3g9-main/build
./tests
```

## Project Structure

```
├── a2_c_refresher_bsn3g9-master/    # C fundamentals (arrays, strings, alloc, bits)
│   ├── allocation/
│   ├── arrays/
│   ├── bits/
│   ├── debug/
│   ├── error_handling/
│   ├── strings/
│   ├── structures/
│   └── system_programming/
├── a3_process_scheduling.sp2025_bsn3g9-main/   # Scheduler sim
├── a3.5-threading_bsn3g9-main/      # Multithreading (pthreads)
├── a4_block_store_bsn3g9-master/    # Block device abstraction layer
└── a5_fs2021_bsn3g9-master/         # inode-based Unix filesystem
```

## License

MIT
