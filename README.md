# Overview

This repository contains the meeting minutes for the RISC-V Virtual Memory task
group, which is currently working on the following tasks:

* Naturally-aligned power-of-two (NAPOT) address translation contiguity
* Attributes (e.g., cacheability) associated with virtual rather than physical
  addresses
* Assorted other updates to the RISC-V virtual memory sections of the RISC-V
  privileged ISA

The documentation is being developed on the
[virtual-memory](https://github.com/riscv/riscv-isa-manual/tree/virtual-memory)
branch of the
[riscv/riscv-isa-manual](https://github.com/riscv/riscv-isa-manual/)
repository, since it is largely a set of small extensions to the existing
privileged ISA specification.

[2020 Member Day Update Video](https://lists.riscv.org/g/allmem/files/Member%20Day%202020/MemberDay2020VirtualMemory.mp4)

# Maintainers

The repository is currently being maintained by the chair and vice-chair of
the virtual memory task group: Daniel Lustig (dlustig@nvidia.com), and Andrea
Mondelli (andrea.mondelli@huawei.com)

# Task Group Status

## Svnapot extension

### Progress towards Stable status
Aiming to complete by end of 2020

* Spec: written, pull request created, reviewed but not merged:
  https://github.com/riscv/riscv-isa-manual/pull/611.
  Snapshots available at https://github.com/riscv/virtual-memory/tree/main/specs.
* Spike update: [merged](https://github.com/riscv/riscv-isa-sim/commit/fce242a5d495db731eee6571916399d10ec531e9)
* Sail formal model: pull request, not reviewed or merged: https://github.com/rems-project/sail-riscv/pull/79
* Tests: currently written only in prose form: [tests.adoc](tests.adoc)
  * These will need to be rewritten in the [proper format](https://github.com/riscv/riscv-compliance)
  * We'll also need a more complete set of tests
  * The architecture test suite and framework are themselves still a work in
    progress, particularly for supervisor and/or Rv64 tests, so we'll have to
    work within those limitations

### Progress beyond Stable status
We'll have to complete the tasks below, but there is no current timeline on
these.

* Full architecture test suite
* Full support in at least one OS
* At least one prototype must be implemented as an ASIC or custom
  placed-and-routed design (e.g., GDSII, not necessarily silicon)

## Assorted minor virtual memory tweaks
These are "fast-track" modifications, and do not have a specific list of tasks
to complete.

* Allow speculative updates of PTE A bit
* Addition of PTE C bit
* Address translation algorithm refactoring
* Slightly relaxed A/D bit update atomicity requirement

## Sv57 Mode
Proposed to be added, and expected to be fast-tracked as well

## Zsa Virtual Address Attributes
In progress, with active discussion in the task group, but no spec yet ready
for review.  A new proposal is under discussion, including:

* attributes definition
* rationale
* interaction with PMA
