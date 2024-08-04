---
layout: post
title: "A Compiler for C89"
date: 2024-08-04 9:30:00 -0400
categories: c compilers projects
---
C, the greatest programming language of all time. This might be a controversial
statement, but hear me out. 
<!--more--> C might not be "memory-safe." It might not have the
most readable syntax. It is too minimal for most intents and purposes. It might
be too close to the hardware for most programmers to understand. But C has more
influence on the world of programming than any other programmer language in
existence. Down to the lowest level, almost everything depends, in one way or
another, at least in some part, on C. Be it a library dependency loaded at
runtime or as part of the OS's system call interface, or even a language's
runtime, C is almost certainly present in any system you can imagine.

Whether C is the *best* programming language is another question altogether,
and I doubt that question is answerable.

So as a token of appreciation of C's greatness, I have decided to write a C
compiler.

# The Constraints

Before I begin to program, I want to be clear about this project's goals. I, like
many programmer's before them, have suffered from the "start a project and don't
finish it" maladie. Setting up more realistic goals is the first step toward
achieving them. So let me set some goalposts:

- My compiler will attempt to conform to the C89/C90 standard.
- The compiler shall target only a *single-threaded* x86\_64 architecture and work
  ONLY with the ELF binary format.
- The compiler will **not** focus on creating a performant compiler, but rather
  a modular one. Each stage of the compilation process should be its own program.
- Code optimization is not a main goal of this project. Correctness is a priority.
- The C standard library shall be implemented, in the simplest, most minimal way
  I can find.
- Error messages should be minimalistic, this compiler is not meant to be used
  for production purposes, only for educational ones.

This seems reasonable. Time to code!
