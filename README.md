
Overview
--------

libsimdpp is a portable header-only zero-overhead C++ wrapper around
single-instruction multiple-data (SIMD) intrinsics found in many compilers. The
library presents a single interface over several instruction sets. In addition
to that, the library allows to compile the same source code for different
instruction sets and seamlessly hook the implementations to an internal dynamic
dispatch mechanism.

The library resolves differences between instruction sets by implementing the
missing functionality as a combination of several intrinsics. Moreover, the
library supplies a lot of additional, commonly used functionality, such as
various variants of matrix transpositions, interleaving loads/stores, optimized
compile-time shuffling instructions, etc. Each of these are implemented in the
most efficient manner for the target instruction set.

The library sits somewhere in the middle between programming directly in
intrinsics and even higher-level SIMD libraries. As much control as possible
is given to the developer, so that it's possible to exactly predict what code
the compiler will generate.

Compiler and instruction set support
------------------------------------

  - This describes the current branch only which may be unstable or otherwise
  unfit for use. For available releases please see the
  [libsimdpp wiki](https://github.com/p12tic/libsimdpp/wiki).

The library supports the following architectures and instruction sets:

 - x86, x86-64: SSE2, SSE3, SSSE3, SSE4.1, AVX, AVX2, FMA3, FMA4, AVX-512F,
XOP
 - ARM, ARM64: NEON

Code for ALTIVEC instruction set has been added, but it has not been tested
on actual hardware, thus definitely contains bugs.

The primary development of the library happens in C++11. A C++98-compatible
version of the library is provided on the
[cxx98](https://github.com/p12tic/libsimdpp/tree/cxx98) branch.

 - C++11 version:
   - GCC: 4.8-5.3
   - Clang: 3.3-3.8
   - MSVC: 2013
   - ICC: 2013, 2015

Clang 3.3 is not supported on ARM. MSVC is only supported on x86-64. ICC is
only supported on x86 and x86-64.

 - C++98 version
   - GCC: 4.4-5.3
   - Clang: 3.3-3.8
   - MSVC: 2013
   - ICC: 2013, 2015

Documentation
-------------

Online documentation is provided
[here](http://p12tic.github.io/libsimdpp/v2.0~beta1/doc/html).

License
-------

The library is distributed under the Boost Software License, Version 1.0

> Boost Software License - Version 1.0 - August 17th, 2003
>
> Permission is hereby granted, free of charge, to any person or organization
> obtaining a copy of the software and accompanying documentation covered by
> this license (the "Software") to use, reproduce, display, distribute,
> execute, and transmit the Software, and to prepare derivative works of the
> Software, and to permit third-parties to whom the Software is furnished to
> do so, all subject to the following:
>
> The copyright notices in the Software and this entire statement, including
> the above license grant, this restriction and the following disclaimer,
> must be included in all copies of the Software, in whole or in part, and
> all derivative works of the Software, unless such copies or derivative
> works are solely in the form of machine-executable object code generated by
> a source language processor.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE, TITLE AND NON-INFRINGEMENT. IN NO EVENT
> SHALL THE COPYRIGHT HOLDERS OR ANYONE DISTRIBUTING THE SOFTWARE BE LIABLE
> FOR ANY DAMAGES OR OTHER LIABILITY, WHETHER IN CONTRACT, TORT OR OTHERWISE,
> ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
> DEALINGS IN THE SOFTWARE.



