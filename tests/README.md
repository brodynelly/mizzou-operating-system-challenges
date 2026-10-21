# Test notes

The assignment directories include different GoogleTest harnesses and CMake targets. There is no repository-wide test executable named `tests`.

For example, A4 defines the `assignment4_test` target:

```sh
cd a4_block_store_bsn3g9-master
cmake -S . -B build
cmake --build build --target assignment4_test
./build/assignment4_test
```

The assignment projects use different target names and some retain course-cluster include or library paths. Check the selected assignment's `CMakeLists.txt` before building. Repository CI currently performs C syntax checks only; it does not run these C++ suites.
