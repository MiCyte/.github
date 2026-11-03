## MiCyte

**A database and its tools, on a machine you control.**

Most software asks you to put your records somewhere else and then rents them back to you.
MiCyte is the other arrangement: the store is yours, it runs where you put it, and the tools
that read it are open source under the **AGPL-3.0**.

### The four repositories, and what each one is for

| | |
|---|---|
| **[MiCyte](https://github.com/MiCyte/MiCyte)** | **the software.** The store, its structures, and the 80-odd tools that read and write it. This is the one you install. It depends on no hosting service and needs no account. |
| **[Gadgets](https://github.com/MiCyte/Gadgets)** | **the apps**, as declarations. An app — Almanac, Brevat, PIM, Quiar — is a named set of tools plus the documents it needs. A declaration **enables; it never adds code**: every tool it names is already in the package you are running. |
| **[TXA](https://github.com/MiCyte/TXA)** | **the taxonomy.** The biological classification tree the growing tools read: what a crop is, what it descends from, and what is known about it. |
| **[Registrar](https://github.com/MiCyte/Registrar)** | **the registry.** How places, entities and administrative regions are addressed, and what is published about them. |

### Why there is no app store here

A declaration is a small JSON file with a digest. Installing from one turns tools on; it cannot
introduce a tool your build does not have, and it grants nothing — what a tool may *write* is a
separate, explicit decision.

That is deliberate. An archive you unpack and run is a code-distribution channel, and a
code-distribution channel without signatures is a supply-chain problem. Until there is a
signing story worth trusting, the thing you can download is the declaration, and the code
arrives the way code should: in a release you can read.

### Where to start

- **Running it** — [MiCyte/MiCyte](https://github.com/MiCyte/MiCyte), `README.md`, then `docs/`.
- **Contributing** — [`docs/CONTRIBUTING.md`](https://github.com/MiCyte/MiCyte/blob/main/docs/CONTRIBUTING.md).
  Read the first section: that repository is a **generated cut**, which changes what a pull
  request means there.
- **Reporting something** — open an issue on the repository it belongs to; the forms ask for
  the one thing bug reports usually leave out.

### A note on what is not here

MiCyte is developed alongside a hosting service that runs instances of it for people who would
rather not run a server. That service's own code is private, and nothing in it is needed to run
MiCyte. The dependency is one-way and there is a test that keeps it that way: the software must
install on a machine that has never heard of the host.
