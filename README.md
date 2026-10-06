# td185721

Independent researcher working on Windows systems programming, binary
analysis, and small reverse engineering tools.

### Current focus

- MSVC / Windows x64 internals — PE/COFF layout, RTTI, class recovery,
  vtable walking
- Low-level C++ tooling for binary inspection and runtime observation
- Self-study in a lab environment: own machines, own target binaries,
  own test harnesses

### Public projects

- **[pe-walker](https://github.com/td185721/pe-walker)** — command-line
  inspector for the Portable Executable format. DOS and NT headers,
  section layout, imports, exports.
- **[pattern-scan](https://github.com/td185721/pattern-scan)** —
  single-header C++17 library for IDA-style byte signature scanning.
  No dependencies, no allocations beyond the parsed signature.
- **[rtti-dump](https://github.com/td185721/rtti-dump)** — MSVC x64 RTTI
  extractor. Recovers class hierarchies from stripped Windows binaries
  by walking the on-disk Complete Object Locator → Class Hierarchy
  Descriptor → Base Class Array chain.
- **[vtable-dump](https://github.com/td185721/vtable-dump)** — companion
  to rtti-dump. Locates class virtual function tables by scanning for
  Complete Object Locator back-references, then enumerates the function
  pointer slots in each vtable.

### Tooling

C++17 / C++20, Rust for standalone utilities, CMake, Ghidra, x64dbg,
WinDbg, MinGW-w64 / MSVC. Occasionally Python for one-off analysis
scripts.

### Interests

Everything that lives between source code and the running process —
object layout, calling conventions, how linkers assemble a binary, how
loaders map it, how debuggers see it, and how to write small tools that
make that visible.
