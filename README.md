# B Programming Language

> [!WARNING]
> The Compiler is not fully implemented yet. Plus on its own it's probably not useful for any serious Software Development. It is fun for Recreational Programming though.

<p align=center>
  <img src="./logo/logo_strawberry.png" width=400>
</p>

<p align=center>
  <sub>Logo by Strawberry 🍓</sub>
</p>

Compiler for the [B Programming Language](https://en.wikipedia.org/wiki/B_(programming_language)) implemented in [Crust](https://github.com/tsoding/crust).

## Dependencies

- [Rust](https://www.rust-lang.org/) - the compiler is written in it;
- [GCC](https://gcc.gnu.org/) or [Clang](https://clang.llvm.org/) (whatever serves as the `cc` on your POSIX platform) - the `x86_64` and `aarch64` targets generate assembly and pass it to `cc` to assemble and link.

<!-- TODO: document specific dependencies for the rest of the targets. Like mingw32-w64 and wine on Linux for gas-x86_64-Windows, etc. -->

## Quick Start

```console
$ make
$ ./build/b -run ./examples/hello_world.b
```

Also check out more examples at [./examples/](./examples/).
Find the project documentation at [./docs/](./docs/).

## Contribution

Accepting Pull Requests is currently paused. We are in the middle of [Decentralizing](https://github.com/tsoding/b/issues/62) this repo. The plan is

1. Create a separate organization for the language.
2. Keep `*x86_64*` and `*aarch64*` codegens in the main repo.
3. Move codegens [6502](./src/codegen/mos6502.rs) (owner [@Miezekatze64](https://github.com/miezekatze64)), [uxn](./src/codegen/uxn.rs) (owner [@deniska](https://github.com/deniska)), [gas-sh4dsp-prizm](https://github.com/tsoding/b/pull/175) (owner [@seija-amanojaku](https://github.com/seija-amanojaku)) to separate repos within the organization and give the owners full admin access to them.

You can still submit PRs in the meantime. Just don't expect them to be reviewed any time soon since decouping codegens requires extensive refactoring. They will be addressed eventually.

## References

- https://en.wikipedia.org/wiki/B_(programming_language)
- https://www.nokia.com/bell-labs/about/dennis-m-ritchie/kbman.html
- https://www.nokia.com/bell-labs/about/dennis-m-ritchie/bref.html
- https://www.nokia.com/bell-labs/about/dennis-m-ritchie/btut.html
