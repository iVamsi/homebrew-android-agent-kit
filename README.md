# homebrew-android-agent-kit

Homebrew tap for [DroidAgentKit](https://github.com/iVamsi/droid-agent-kit) — an Android
development MCP server giving AI coding agents real Android tools (Gradle, adb, logcat, lint,
crash triage, Perfetto) through a local, permissioned server instead of raw shell access.

```bash
brew install iVamsi/android-agent-kit/droidagent
```

Then register it with your agent:

```bash
droidagent install-mcp
droidagent doctor      # if anything misbehaves, start here
```

## Formula maintenance

`Formula/droidagent.rb` is **generated, not hand-edited**. The release workflow in the main
repository runs `scripts/generate-homebrew-formula.sh`, which pins the SHA-256 from the release's
own published `.sha256` asset, and pushes the result here.

To regenerate manually:

```bash
scripts/generate-homebrew-formula.sh <version> Formula/droidagent.rb
```
