# SSH2FA — Homebrew Tap

Homebrew tap for [**SSH2FA**](https://github.com/gasvn/ssh2fa) — a macOS menu-bar
app that keeps SSH ControlMaster connections warm to Duo / TOTP-gated hosts and
answers the 2FA login for you, so you log in once and stay connected.

## Install

```sh
brew install --cask --no-quarantine gasvn/tap/ssh2fa
```

> **Why `--no-quarantine`?** SSH2FA isn't notarized yet (that's the
> [$99 Apple Developer goal](https://shgao.site/ssh2fa/#support)). The flag tells
> Homebrew to skip the macOS Gatekeeper quarantine, so the app opens with no
> "unverified developer" warning. Without it, the first launch is blocked — allow
> it once via **System Settings → Privacy & Security → "Open Anyway."**

## Update / uninstall

```sh
brew upgrade --cask ssh2fa            # update to the latest release
brew uninstall --cask ssh2fa          # remove the app
brew uninstall --zap --cask ssh2fa    # also wipe saved hosts + Keychain creds
```

## More

- Website: <https://shgao.site/ssh2fa/>
- Source & releases: <https://github.com/gasvn/ssh2fa>
