# SSH2FA — Homebrew Tap

Homebrew tap for [**SSH2FA**](https://github.com/gasvn/ssh2fa) — a macOS menu-bar
app that keeps SSH ControlMaster connections warm to Duo / TOTP-gated hosts and
answers the 2FA login for you, so you log in once and stay connected.

## Install

```sh
brew install --cask gasvn/tap/ssh2fa \
  && xattr -dr com.apple.quarantine /Applications/SSH2FA.app \
  && open /Applications/SSH2FA.app
```

> **Why the extra steps?** SSH2FA isn't notarized yet (that's the
> [$99 Apple Developer goal](https://shgao.site/ssh2fa/#support)), so Homebrew
> quarantines it on install and macOS blocks the first launch. The `xattr` line
> clears that flag so it opens with no "unverified developer" warning — or just
> allow it once via **System Settings → Privacy & Security → "Open Anyway."**
> (Don't use the old `--no-quarantine` install flag — newer Homebrew removed it.)

## Update / uninstall

```sh
brew upgrade --cask ssh2fa            # update to the latest release
brew uninstall --cask ssh2fa          # remove the app
brew uninstall --zap --cask ssh2fa    # also wipe saved hosts + Keychain creds
```

## More

- Website: <https://shgao.site/ssh2fa/>
- Source & releases: <https://github.com/gasvn/ssh2fa>
