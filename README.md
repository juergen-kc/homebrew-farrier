# Homebrew tap for Farrier

[Farrier](https://github.com/juergen-kc/farrier) keeps your Mac sound from the command line and from AI agents (MCP):
posture checks, fixes you approve on the Mac, and a journal of what changed.

```bash
brew install --cask juergen-kc/farrier/farrier
```

Then, as yourself:

```bash
farrier helper register   # allow Farrier in System Settings → General → Login Items
farrier setup             # the approval key (an admin dialog appears)
```

The cask installs `Farrier.app` owned by root and a `farrier` wrapper on your PATH. `brew uninstall --cask farrier`
removes the helper registration, the approval key, the app and the wrapper; `brew uninstall --zap --cask farrier`
also removes the journals, plans and exceptions.

`Casks/farrier.rb` is updated by Farrier's release workflow; please open issues in the
[main repository](https://github.com/juergen-kc/farrier/issues).
