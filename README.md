# memory_mesh / Michael Ouse

Michael Ouse — a Rust project in miniature.

A tiny, whimsical Rust program that models non-binary epistemic states for a woodland rodent and emits narrative telemetry. It prints a decorative header, a short telemetry block, and a letter from Michael Ouse, then persists its runtime state to `michael_memory.json` using serde.

Why this exists

- To explore small runtime models of uncertainty (not just booleans).
- To produce readable narrative telemetry and persist it for later inspection.
- To provide a compact, hackable Rust project you can fork and extend.

Quick start

1. Clone the repo:

   git clone https://github.com/emmatoad-droid/michael_ouse.git
   cd michael_ouse

2. (Optional) If you prefer the `cargo add` workflow to add dependencies locally:

   # install cargo-edit if you don't have it
   cargo install cargo-edit

   # then run these (not necessary if the repo already contains Cargo.toml):
   cargo add serde --features derive
   cargo add serde_json

3. Build and run:

   cargo build
   cargo run

4. After running, check `michael_memory.json` in the project root — it contains the persisted state.

Example output (abridged)

=== MEMORY MESH TELEMETRY ===
Execution Count:           1
Fox Loneliness:            CERTAIN
Beetle Boolean Casting: COMPLETE NONSENSE
Walnut Memory Buffer:      6 units
----------------------------------

+-------------------------------------------------------+
Dear Emma,
...
Persistence: Logged to michael_memory.json (Execution #1)
+-------------------------------------------------------+

Publishing to crates.io (optional)

- Ensure `Cargo.toml` contains metadata fields: `name`, `version`, `description`, `license` or `license-file`, `readme`, `repository`.
- Test packaging locally:

  cargo package

- Create a crates.io API token and authenticate: `cargo login <TOKEN>`
- Publish: `cargo publish`

Notes & suggestions

- The repo includes `serde` and `serde_json` in `Cargo.toml`. You can run the program as-is.
- `michael_memory.json` is listed in `.gitignore` by default. If you want persisted runs tracked, remove it from `.gitignore` before committing.
- Add tests: a simple serde round-trip test is a good first change.
- Add GitHub Actions CI to run `cargo build --verbose` and `cargo test --verbose` on push/PR.

License

This project is MIT-licensed — see LICENSE.

Contact

https://github.com/emmatoad-droid/michael_ouse
