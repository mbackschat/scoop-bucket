# Martin Backschat's Scoop bucket

Add the bucket once:

```powershell
scoop bucket add mbackschat https://github.com/mbackschat/scoop-bucket
```

## locmetry

[locmetry](https://github.com/mbackschat/locmetry) measures lines of code with embedded Tokei and classifies every file as production, test or other by reviewable project rules.

Requires Windows on x86_64. Install the prebuilt release without a Rust toolchain:

```powershell
scoop install mbackschat/locmetry
locmetry --format markdown
```

Update with:

```powershell
scoop update
scoop update locmetry
```

Scoop verifies the release archive's SHA-256 checksum. The optional `compare-locmetry-files.sh` helper is installed next to the executable and needs Bash, for example from Git for Windows, and `jq` (`scoop install jq`).

## Maintaining the manifests

For a new locmetry release, render [its manifest](bucket/locmetry.json) with `packaging/scoop/render-manifest.sh VERSION` from the locmetry repository, which fills the URL and checksum from the release's `SHA256SUMS`. Check that the JSON parses and that the hash matches the release before pushing.

## License

[MIT](LICENSE).
