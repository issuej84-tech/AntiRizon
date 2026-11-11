# AntiRizon

Native Rust launcher and client for Minecraft Java 26.3. Version **1.0.0-dev.1**.

## Download

Open [Releases](https://github.com/issuej84-tech/AntiRizon/releases/tag/antirizon-v1.0.0-dev.1). Assets:

- `AntiRizon-1.0.0-dev.1-linux-x86_64.tar.gz` — Linux launcher and optimized client.
- `AntiRizon-1.0.0-dev.1-source.tar.gz` — complete source tree for this fork.
- Matching `.sha256` files — archive checksums.

Extract the Linux archive, open its folder and run `./AntiRizon`. Keep
`antirizon-client` beside the launcher. The first resource preparation needs internet;
Minecraft resources and JARs are not included. Change the offline nickname in the profile menu.

## Source and build

Extract the source archive and run from its root:

```sh
cargo build --locked --release --manifest-path launcher/Cargo.toml --bin horizon-launcher
cargo build --locked --profile fast -p horizon-client
```

Rust 1.95+ and native platform dependencies are required; see `FORK-SAM.md` and
`docs/antirizon-linux.md` in the source archive. Technical Cargo names and data formats
remain compatible. Linux was built and smoke-tested; Windows/macOS builds are unverified.

## Features and limits

Editable offline profile, custom launcher design and branding, optimized Linux build,
and an experimental converter for a subset of static Java logic. The converter does not
automatically produce playable Minecraft mods. Online-mode servers require a valid account.

## Origin and license

Based on [horizon-rust/horizon](https://github.com/horizon-rust/horizon), original commit
`1405044d0996d37f850f5ab0dec02bab43d4945f`. Original copyright and third-party notices
are preserved in the archives. See [LICENSE](LICENSE).
