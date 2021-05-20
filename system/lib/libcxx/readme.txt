These files are from libc++, release branch 10.x.

tag: llvmorg-12.0.0
git: d28af7c654d8db0b68c175db5ce212d74fb5e9bc

Update Instructions
-------------------

Run `system/lib/update_libcxx.py path/to/llvm-project`

Local Modification
------------------

Local modifications are marked with the comment: 'XXX EMSCRIPTEN'

1. Define _LIBCPP_HAS_THREAD_API_PTHREAD in libcxx/__config./

2. Define _LIBCPP_ELAST in libcxx/include/config_elast.h

3. Use _LIBCPP_USING_GETENTROPY (like wasi)

4. Undefine _LIBCPP_ABI_OPTIMIZED_FUNCTION
   See https://github.com/emscripten-core/emscripten/issues/11022

5. Don't define _LIBCPP_HAS_CATOPEN

6. src/new.cpp: Abort on malloc failure when exceptions are disabled.

7. include/typeinfo: add always_inline to type_info::operator==
   See  https://github.com/emscripten-core/emscripten/issues/13330
