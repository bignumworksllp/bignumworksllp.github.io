**Slide - Section Introduction**

Welcome to Section - Threading and Multiprocessing

In this section we will learn about Threading and Multiprocessing in
Python.

**Slide - Video Introduction**

Welcome to the video - Doing asynchronous work (short intro/concurrency)

In this video, we are going to learn:

-   Evolution of Computing Hardware, more specifically the Moore's law.

-   Advancement of OSes to support concurrency where we disucss about
    the various abstracts or constructs the OS has to support
    concurrency.

-   **Programmer’s Interface to Concurrency where we discuss in little
    detail how programmers can use the Operating system's concurrency
    constructs.**

So, lets start with the first topic then.

**Slide - Evolution Of Computing Hardware**

**Let's discuss a famous observation...**

**Moore's Law:**

This is often considered as the motivation for the evolution of
concurrency. Moore's law is often considered as an observation or
projection rather than a physical or a natural law is named after Gordon
E Moore, who in his 1965 paper observed that the number of
[transistors](https://en.wikipedia.org/wiki/Transistor) in a dense
[integrated circuit](https://en.wikipedia.org/wiki/Integrated_circuit)
doubles approximately every two years. The meaning of this is that the
processing power of a computer would double every two years.

Gordon Moore went on to become the co-founder of Intel which pioneered
the development of integrated circuits, computer processors championing
the Moore's law for more than a few decades and not just for a decade
which Moore predicted the phenomenon would last for.

The law has formed the guiding light for the semi-conductor industry in
the long-term planning and to set targets for [research and
development](https://en.wikipedia.org/wiki/Research_and_development).
Advancements in digital electronics are strongly linked to Moore's law
[quality-adjusted](https://en.wikipedia.org/wiki/Price_index#Quality_change)
microprocessor prices, [memory
capacity](https://en.wikipedia.org/wiki/Random-access_memory),
[sensors](https://en.wikipedia.org/wiki/Digital_sensor) and even the
number and size of [pixels](https://en.wikipedia.org/wiki/Pixel) in
[digital cameras](https://en.wikipedia.org/wiki/Digital_camera).

**Slide – MultiCore Processor**

How did the processing power manifest as? Not only did the clock speed
of the processor became fast, Instead of a single processor core, the
processor/chip companies started designing and implementing processors
with multiple cores with each core capable of executing instructions
simultaneously without interfering or depending on the other cores.

This meant that multiple tasks could be run at the same time on
processors concurrently and that if only one task is run then the
remaining cores would be idle. To successfully leverage the processing
power of the processor, we must be able to build tasks that can run
concurrently and go to completion without any issues.

A footnote on Moore's law:

In 2015 Gordon Moore foresaw that the rate of
[progress](https://en.wikipedia.org/wiki/Exponential_growth) would reach
[saturation](https://en.wikipedia.org/wiki/Logistic_function) and I
quote him here: "I see Moore's law dying here in the next decade or so."
In the same year Intel announced that the cadence is two and half years
for doubling rather than two years and also said that the Moore's law
would continue to hold indefinitely.

**Slide - Operating system support for concurrency:**

We now know that the processors evolved to support concurrent tasks. To
be able to use this capability, the operating systems evolved too. The
primary capability of the operating system to be able to perform
multiple tasks also has come a long way.

To be able to perform multiple unrelated tasks at the same time or
splitting the same task into multiple subtasks to be able to run at the
same time independently, the operating system has to provide constructs.
Not just these constructs but a whole infrastructure has to be built
around these constructs to be able to run multiple tasks concurrently.

Two such constructs are : Processes and Threads. These form the building
blocks of concurrency.

A process is basically a program in execution and can have one or more
threads running at the same time.

Just these abstractions are not enough to be able to bring in
concurrency. Each process/thread should be able to get a chance to run
on the processor. So, the Operating System should be able to schedule
processes for execution using some method.

A process should be able to be protected from other processes and so
should have separate memory. Also, the threads within a process should
be able to share this memory. This lead to the concept of Virtual
Memory.

Each process might be need to communicate with each other. Operating
system should be able to support such inter process communication. This
is done using mechanisms such as Message Passing and Shared Memory.

Also, for the threads of the same process or different processes should
be able to synchronously share data without any side-effects such as
deadlocks. To facilitate this, the Operating systems provide various
synchronization mechanisms such as Semaphores, mutexes, critical
sections etc.

**Supporting the Programmer’s Interface to Concurrency**

**(Source:**
<http://repository.cmu.edu/cgi/viewcontent.cgi?article=1180&context=sei>**)**

Operating systems supporting concurrency is not enough. Programmers
should be able use the supporting infrastructure to be able to build
concurrent applications. This can be achieved in three ways.

1\. Libraries of supervisor calls to proprietary operating systems. (IBM
Main Frames instructions and are pretty old.). These are typically done
using assembly language and are tied closely to the Hardware and hence
difficult to extend.

2\. Special (syntactically distinct) language constructs, independent of
the operating system or target computer. Examples include Concurrent
programming languages such as Concurrent C. Though this can achieve the
portability, maintainability and abstraction, the problem is a rigid set
of language semantics which cannot be changed easily as it would require
changes to the compiler itself.

3\. Language constructs at the semantic level only; that is, subroutine
libraries in programming languages such as Python, Java etc supporting
process types and operations, independent of the operating system or
target computer. This is the one we are interested in for this course.

With this approach, no special syntactic structures are imposed on the
language. Instead, a library or module supports concurrency by defining
types (process, for example), and operations in the form of subprograms
that can be called from an application. The programmer interface to such
modules is machine- and system-independent; the implementation of the
modules, of course, depends upon the underlying operating system and
hardware.

**Slide - Video - Conclusion**

In this video, we learned

-   Evolution of Computing Hardware

-   Advancement of OSes to support concurrency.

Programming languages support for Concurrency.

In the next video, we will…

**------------------------- end ---------------------**
