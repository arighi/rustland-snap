## Overview

`scx_rustland` is Linux scheduler based on
([`sched_ext`](https://github.com/sched-ext/scx).

It is made of a BPF component (dispatcher) that implements the low level
sched-ext functionalities and a user-space counterpart (scheduler), written in
Rust, that implements the actual scheduling policy.

The scheduler is designed to prioritize interactive workloads over background
CPU-intensive workloads. For this reason the typical use case involves
low-latency interactive applications, such as gaming, video conferencing and
live streaming.

This repository contains the snap packaging configuration (`snapcraft.yaml`)
used to create a snap from the Rust crate published on crates.io.

## Requirements

In order to use `scx_rustland` you need to install the latest Ubuntu kernel
from this ppa:

  https://launchpad.net/~arighi/+archive/ubuntu/sched-ext

## Source repository

The source code of `scx_rustland` is available in the
[scx](https://github.com/sched-ext/scx) repository.
