---
title: "myTransferApp"
excerpt: "Command-line file transfer app for Linux in C, using sockets, multiprocessing and multithreading. Operating Systems course project."
collection: portfolio
order: 1
kind: university
---

<p><a href="https://github.com/DanieleMarche/myTransferApp" class="btn btn--primary"><i class="fab fa-github" aria-hidden="true"></i> View on GitHub</a></p>

myTransferApp is a command-line application for Linux that transfers files between two computers. I built it for the **Operating Systems** course at Sapienza.

The project uses low-level OS primitives directly:

- **Sockets** for client–server communication over the network
- **Multiprocessing and multithreading** so several transfers can run concurrently
- **Dynamic memory allocation**, managed by hand, for the file buffers

<hr>

### Technologies used

- **Language:** C
- **Platform:** Linux (POSIX sockets, `fork`, pthreads)
