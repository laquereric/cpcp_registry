# cpcp_registry — method and seam registries, naming and versioning

The machine-readable index of the CPCP contract: which methods exist,
which seams serve them, under what names and versions.

## Naming & versioning

| Form | Meaning |
|---|---|
| `JSON-RPC-LD-PS1` | the standard |
| `JSON-RPC-LD-PS1-P{N}` | the CPCP repo for Profile N (its own Git repo) |
| `JSON-RPC-LD-PS1-P{N}.{VV}` | a **labeled SHA** (a Git tag) pinning a specific commit of that CPCP repo |

These identifiers are unchanged by renames. `PS1` remains the standard's
name; `CPCP` names what a package of it is. A labeled SHA is how a
consumer pins: method registries drift, tags do not move.

## Contents

* `registry.json` — profile entries. Entries appear here when their
  repositories are public and stable — no dead links are listed.
* `registry/methods.json` — every served method: wire identity,
  direction parties, shapes, refusals, profiles. Entries flagged
  `native` belong to the demo seam, not an extraction.
* `registry/seams.json` — live seams, authority, and layer bindings.

Refusals, envelopes, and HTTP mapping live in the
[contract repo](https://github.com/laquereric/coordination-protocol-contract-package)
(`spec/`); runnable clients and the demo live in
[cpcp_demo](https://github.com/laquereric/cpcp_demo).
