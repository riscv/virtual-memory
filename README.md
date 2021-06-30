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

PDFs of all spec drafts are available at the following link:
https://github.com/riscv/virtual-memory/tree/main/specs.

## Assorted minor virtual memory tweaks

Draft available:
https://github.com/riscv/riscv-isa-manual/pull/611

To be merged into master and reviewed as part of Priv 1.12.

* Sv57 added
* Allow speculative updates of PTE A bit
* Addition of PTE C bit
* Address translation algorithm refactoring
* Slightly relaxed A/D bit update atomicity requirement

## Svnapot: Naturally-Aligned Power-of-Two Address-Translation Contiguity

Draft available:
https://github.com/riscv/riscv-isa-manual/pull/628

### Progress towards Stable status

Working through the RISC-V review process.

* Spec: written, pull request created, reviewed but not merged:
  https://github.com/riscv/riscv-isa-manual/pull/628.
  Snapshots available at https://github.com/riscv/virtual-memory/tree/main/specs.
* Spike update: [merged](https://github.com/riscv/riscv-isa-sim/commit/fce242a5d495db731eee6571916399d10ec531e9)
* Sail formal model: pull request, not reviewed or merged: https://github.com/rems-project/sail-riscv/pull/79
* Tests: currently written only in prose form: [tests.adoc](tests.adoc)
  * These will need to be rewritten in the [proper format](https://github.com/riscv/riscv-compliance)
  * We'll also need a more complete set of tests
  * The architecture test suite and framework are themselves still a work in
    progress, particularly for supervisor and/or Rv64 tests, so we'll have to
    work within those limitations

## Svpbmt: Page-based Memory Types

First draft now available
https://github.com/riscv/riscv-isa-manual/pull/663

## Svinval: Fine-Grained Address-Translation Cache Invalidation

First draft now available
https://github.com/riscv/riscv-isa-manual/pull/668

## Progress beyond Stable status
For all of these extensions we'll have to complete the "Definition of Done" tasks,
including those below, but there is no current timeline on these.

* Full architecture test suite
* Full support in at least one OS
* At least one prototype must be implemented as an ASIC or custom
  placed-and-routed design (e.g., GDSII, not necessarily silicon)
