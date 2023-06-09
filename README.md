# hpackage-rs

Rust client package for Hollow Knight PackageDefs. Types are generated from the schema at https://github.com/hpackage/hpackage-schema using [typify](https://crates.io/crates/typify); see the docs for more details on the generated types.

Consumers may use the `parse_validate` function to validate and parse an input, but the generated types all play nicely with
`serde_json` if you'd rather skip validation or do it yourself. Because of the structure of the generated Rust data types, there is no need to post-validate generated output; a normal write via `serde_json` will produce a valid package definition.
