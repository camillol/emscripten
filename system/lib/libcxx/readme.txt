These files are from llvm-project/libcxx, release branch 10.x.

tag: llvmorg-10.0.0
git: d32170dbd5b0d54436537b6b75beaf44324e0c28

Update Instructions
-------------------

Run `system/lib/update_libcxx.py path/to/llvm-project`

Local Modification
------------------

The differences from upstream libc++ are stored in our fork of llvm.  The
changes from upstream can seen by comparing the `llvmorg-10.0.0` and
emscripten-libs-10.0.0` branches:

https://github.com/llvm/llvm-project/compare/llvmorg-10.0.0...emscripten-core:emscripten-libs-10.0.0
