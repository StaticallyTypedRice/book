What Redox is
=============

Redox is a general purpose operating system and surrounding ecosystem written in pure [Rust]. Our aim is to provide a fully functioning Unix-like microkernel, that is both secure and free.

We have modest compatibility with [POSIX], allowing Redox to run many programs without porting.

We take inspiration from [Plan9], [Minix], [Linux], and [BSD]. We are trying to generalize various concepts from other systems, to get one unified design. We will speak about this some more in the [Design] chapter.

At this time, Redox supports:

* All x86-64 CPUs.
* Graphics cards with VBE support (all Nvidia, Intel, and AMD cards from the past decade have this).
* AHCI disks.
* E1000 or RTL8168 network cards.
* Intel HDA audio controllers.
* Mouse and keyboard with PS/2 emulation.

This book is broken into 9 parts:

- [Overview]: A quick'n'dirty overview of Redox.
- [Introduction]: Explanation of what Redox is and how it compares to other systems.
- [Getting started]: Compiling and running Redox.
- [The design]: An in-depth introduction to the design and implementation of Redox.
- Development in user space: Writing applications for Redox.
- [Contributing]: How you can contribute to Redox.
- Understanding the codebase: For familiarizing yourself with the codebase.
- Fun: Top secret chapter.
- The future: What Redox aims to be.

It is written such that you do not need any prior knowledge in Rust and/or OS development.

[Rust]:  https://www.rust-lang.org
[POSIX]: https://en.wikipedia.org/wiki/POSIX
[Plan9]: http://9p.io/plan9/index.html
[Minix]: http://www.minix3.org/
[Linux]: https://en.wikipedia.org/wiki/Linux
[BSD]: http://www.bsd.org/

[Design]: ../design/design.html
[Overview]: ./welcome.html
[Introduction]: ../introduction/why_redox.html
[Getting started]: ../getting_started/preparing_the_build.html
[The design]: ../design/design.html
[Contributing]: ../contributing/chat.html
