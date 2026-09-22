# homebrew-tap

Homebrew tap for [TSLink](https://github.com/monody0007/tslink), a Tailscale-backed gateway that gives any local service its own tailnet hostname with one command.

## Install

```bash
brew install --cask monody0007/tap/tslink
```

The cask installs the `tslink` binary and removes the `com.apple.quarantine` attribute Homebrew stamps on the download: the binary is ad-hoc signed and not notarized, and without that step macOS Gatekeeper blocks its first run. Homebrew casks are macOS-only; on Linux use the `.deb` / `.rpm` / `.tar.gz` assets from the [releases page](https://github.com/monody0007/tslink/releases) or `go install github.com/monody0007/tslink@latest`.

## How this tap is maintained

`Casks/tslink.rb` is generated and pushed by the TSLink release workflow (GoReleaser `homebrew_casks`) on every stable tag. Do not edit it by hand; changes belong in the [tslink](https://github.com/monody0007/tslink) repository's `.goreleaser.yml`.

## License

The cask definition in this repository is released under the [Apache License 2.0](./LICENSE). TSLink itself is licensed separately in its own repository.
