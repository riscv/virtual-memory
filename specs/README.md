# Virtual Memory Task Group Draft Specifications

This folder contains pre-built PDFs of draft specification updates being
developed by the RISC-V virtual memory task group.

Files are named in one of the following ways:

* `<PR>-<branchname>.pdf`: for branches with open pull requests at
  https://github.com/riscv/riscv-isa-manual/
* `<PR>-<branchname>-diff.pdf`: like above, except the PDF highlights the
  differences between this branch and the previous spec (as determined
  automatically using latexdiff)
* `<branchname>.pdf` and `<branchname>-diff.pdf`: like above, except with
  branches that do not yet have an open pull request

Although each draft is organized as a series of incremental changes to the
previous (e.g., Svpbmt is built on top of Svnapot) for convenience, each
extension should be treated as a separate, independent entity for the purposes
of review and ratification.
