# PaperReading

* 05/31/2020 [Deep Sets](https://arxiv.org/pdf/1703.06114.pdf)
```
A function f(X) is invariant to the permutation of instances in X iff it can be decomposed in the form of 
- a neural net \rho(.) on top of summation of the transform \phi(x) applied to each component in a set
```
* 06/28/2020 [MA-DNN](https://arxiv.org/pdf/1907.04667.pdf)
```
we create two external memory vectors for each user, memorizing high-level abstractions of what a user possibly likes and dislikes. 
The proposed MA-DNN achieves a good compromise between DNN and RNN. It is as simple as DNN, but has certain ability to exploit useful information contained in users’ historical behaviors as RNN.
Learn two user-level embeddings for label 0/1 separately, feed into dense together with other groups' embedding vectors. Pose an additional L2 loss to force the two embeddings close to last layer of DNN. This loss only updates the two embeddings(last layer only updated in cross-entropy loss).
```
* 07/06/2020 [MoSE](https://research.google/pubs/pub49274/)
```
Recently, using neural sequence models to effectively represent users’ activity streams has become popular in web applications.
The work in [3](https://research.google/pubs/pub46488/) studies how to effectively use context features(such as device) for recommending videos in Youtube. It uses LSTM to represent a user’s video watch history. 
[30](https://www.ismll.uni-hildesheim.de/pub/pdfs/RendleFreudenthaler2010-FPMC.pdf) is a personalized sequential recommendation model based on Markov chains. 
[39] applies a Recurrent Neural Network (RNN) for next basket recommendation.(https://cseweb.ucsd.edu/classes/fa17/cse291-b/reading/A%20Dynamic%20Recurrent%20Model%20for%20Next%20Basket%20Recommendation.pdf)
[33](https://arxiv.org/abs/1902.08588) uses RNN and Attention to model both short and long range dependencies in user sequences. 
[17](https://arxiv.org/abs/1808.09781) proposes a self-attention based sequential model for next item recommendation[13] shows that RNN can learn multiple user dynamics patterns in individual recommendation sessions.
```
* 07/06/2020 [Deep Learning for Sequential Recommendation](https://arxiv.org/pdf/1905.01997.pdf)

Queue:
[MOE](https://arxiv.org/abs/1701.06538)
[ExplorationStrategiesInDL](https://lilianweng.github.io/lil-log/2020/06/07/exploration-strategies-in-deep-reinforcement-learning.html)
[RoBERTa](https://arxiv.org/abs/1907.11692)
[FaceNet](https://arxiv.org/abs/1503.03832)
[IntegratedGradient](https://arxiv.org/abs/1703.01365)
[VideoBERT](https://arxiv.org/abs/1904.01766)

# System
* Pinterest Engineering [Blog](https://medium.com/@Pinterest_Engineering/the-top-pinterest-engineering-blog-posts-of-2019-51a3bef4a816)
* Lil's [Blog](https://lilianweng.github.io/lil-log/)
* [System Design Primer](https://github.com/donnemartin/system-design-primer)


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
* [Python Cheatsheet](https://gto76.github.io/python-cheatsheet/)
