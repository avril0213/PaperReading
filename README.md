# PaperReading

* 05/31/2020 [Deep Sets](https://arxiv.org/pdf/1703.06114.pdf)
```
A function f(X) is invariant to the permutation of instances in X iff it can be decomposed in the form of 
- a neural net \rho(.) on top of summation of the transform \phi(x) applied to each component in a set
```
* 06/28/2020 [MA-DNN](https://arxiv.org/pdf/1907.04667.pdf)

Queue:
[MOE](https://arxiv.org/abs/1701.06538)
[ExplorationStrategiesInDL](https://lilianweng.github.io/lil-log/2020/06/07/exploration-strategies-in-deep-reinforcement-learning.html)
[RoBERTa](https://arxiv.org/abs/1907.11692)
[FaceNet](https://arxiv.org/abs/1503.03832)
[IntegratedGradient](https://arxiv.org/abs/1703.01365)

# System
* Pinterest Engineering [Blog](https://medium.com/@Pinterest_Engineering/the-top-pinterest-engineering-blog-posts-of-2019-51a3bef4a816)
* Lil's [Blog](https://lilianweng.github.io/lil-log/)


# Coding
* Memory management: [C++ ownership semantics](http://ericlavesson.blogspot.com/2013/03/c-ownership-semantics.html), [RAII-idiom](https://en.wikipedia.org/wiki/Resource_acquisition_is_initialization), [std::lock_guard](https://en.cppreference.com/w/cpp/thread/lock_guard)
```
unique_ptr encapsulates a raw pointer and can't be copied. Trying to assign one unique_ptr to another will give a compile error. It basically replaces the deprecated auto_ptr, but which much clearer semantics. A pointer of this type CAN be moved though, meaning that it gives up ownership of its inner pointer to another unique_ptr instance. This has to be done explicitly by the developer by using std::move.
As opposed to unique_ptr, shared_ptr can be copied. It involves somewhat more overhead since it relies on reference counting. Everytime a shared_ptr runs out of scope, the reference counter goes down. Or, in the case of 0 references, the pointer is deleted.
```
* Compile and Link: [Static Library vs. Shared Library](https://www3.ntu.edu.sg/home/ehchua/programming/cpp/gcc_make.html)
```
A library is a collection of pre-compiled object files that can be linked into your programs via the linker. Examples are the system functions such as printf() and sqrt().
There are two types of external libraries: static library and shared library.
A static library has file extension of ".a" (archive file) in Unixes or ".lib" (library) in Windows. When your program is linked against a static library, the machine code of external functions used in your program is copied into the executable. A static library can be created via the archive program "ar.exe".
A shared library has file extension of ".so" (shared objects) in Unixes or ".dll" (dynamic link library) in Windows. When your program is linked against a shared library, only a small table is created in the executable. Before the executable starts running, the operating system loads the machine code needed for the external functions - a process known as dynamic linking. Dynamic linking makes executable files smaller and saves disk space, because one copy of a library can be shared between multiple programs. Furthermore, most operating systems allows one copy of a shared library in memory to be used by all running programs, thus, saving memory. The shared library codes can be upgraded without the need to recompile your program.
Because of the advantage of dynamic linking, GCC, by default, links to the shared library if it is available.
```
