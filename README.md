# Breez Mobile Client

<p align='center'>
  <img src='https://breez.technology/balance-illustration.webp' height='300' alt='screenshot' />
  <img src='https://breez.technology/pos-illustration.webp' height='300' alt='screenshot' />
  <img src='https://breez.technology/podcast-illustration.webp' height='300' alt='screenshot' />
</p>

[Breez](https://breez.technology) is a Lightning Network [mobile client](https://github.com/breez/breezmobile) and a [hub](https://github.com/breez/server). It provides a platform for simple, instantaneous bitcoin payments. <br>
Breez is currently in a public beta, available on [Android](https://play.google.com/apps/testing/com.breez.client) and on [iOS](https://testflight.apple.com/join/wPju2Du7). <br>
To learn more about it, please read [Introducing Breez](https://doc.breez.technology). <br>

## Features

- [x] lnd on Android
- [x] Neutrino on Android
- [x] Seamless hub channel creation
- [x] Adding funds using on-chain tx
- [x] BTC & Satoshi units
- [x] Random avatars
- [x] Connect to Pay: simple interface to execute payments between users
- [x] A full lncli interface to query and execute ln commands
- [x] Filter tx by type
- [x] Filter tx by date
- [x] Pay invoice (link or QR) from other ln wallets
- [x] Create invoice (link or QR) to be paid by other ln wallets
- [x] Removing funds to an on-chain address
- [x] SubmarineSwaps for adding on-chain funds including refund functionality
- [x] End-to-end encryption of Connect-to-Pay session
- [x] Make Connect-to-Pay links work for users that didn't yet install Breez
- [x] Ability to Backup/Restore the ln node  
- [x] Mainnet support
- [x] Support zero-sat invoices
- [x] Startup optimizations
- [x] Background sync via FCM
- [x] Marketplace w/ Bitrefill
- [x] Adding funds via vouchers
- [x] Backup improvements
- [x] Add background ChannelsWatcher job
- [x] Expose Bitcoin Node (BIP157) configuration
- [x] iOS support
- [x] Add webLN support
- [x] Fiat units
- [x] Optional PIN
- [x] Adding funds via credit card
- [x] Add stronger encryption to cloud backup
- [x] iCloud backup option
- [x] Dark mode
- [x] Export payments to .csv
- [x] Support 3rd-party LSPs
- [x] Biometric login
- [x] Fast onboarding
- [x] Pay w/o full sync
- [x] Implement lnurl-withdraw 
- [x] Send on-chain via reverse Submarine Swaps
- [x] Improve hodl invoice support
- [x] POS POC release
- [x] Spontaneous payments to node id (nodes running with --accept-keysend)
- [x] Fast graph sync
- [x] Scan QR code from an image
- [x] Import/export POS items
- [x] Support zero-conf channels
- [x] 'On-the-fly' channel creation (increase limit)
- [x] Remove reserve working using Breez channels
- [x] Support additional fiat currencies
- [x] Support LNURL-Auth & LNURL-Fallback
- [x] Print POS transactions
- [x] Hide balance
- [x] Read NFC tags on Android
- [x] In-app podcast player (podcasting 2.0)
- [x] Backup to WebDav servers (e.g. Nextcloud)
- [x] Support LNURL-Pay ([bounty redeemed](https://github.com/breez/breezmobile/wiki/Bounties#lnurl-pay-support))
- [x] Send to a Lightning address
- [x] Boostagrams
- [x] WebDav backups 
- [x] Sales reports
- [x] Top podcasts
- [x] NFC checkout 
- [x] Tor support (Android)
- [x] Neutrino sync optimizations
- [ ] Async payments

## System Requirements
* Android 7+ 64bit
* iPhone 6+

## Setting up the environment

### Prerequisites

Make sure you have Flutter 3 installed on your system before continuing the setup process.

### Setting up for Android

1. Build `breez.aar` as described in https://github.com/breez/breez
2. Create a symlink from the `breez.aar` to `android/app/libs` directory.
3. Create an Android app on [Firebase](https://console.firebase.google.com/) and download `google-services.json` file.
  - **Package name (for debugging):** com.breez.client.debug
4. Copy the downloaded `google-services.json` file to `android/app/src/client` folder.

### Setting up for iOS

1. Build and `bindings.framework` as described in https://github.com/breez/breez
2. Copy the `bindings.framework` directory to the ios directory.
3. Create an iOS app on [Firebase](https://console.firebase.google.com/) and download `GoogleServices-info.plist` file.
4. Copy the downloaded `GoogleServices-info.plist` file to `ios` folder.
5. Run `pod install` from `breezmobile/ios`

## Building and Running

```sh
# Install dependencies for building
flutter pub get

# Run a client app on the connected device
flutter run --flavor=client

# Build a client app as APK file
flutter build apk --target-platform=android-arm64 --flavor=client --debug
```

## [Overview for Developers](https://doc.breez.technology/Overview-for-Developers.html)
## [Running Breez in simnet](https://doc.breez.technology/Running-Breez-in-simnet.html)
