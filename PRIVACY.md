# Privacy Policy for PriceFuse

Last updated: September 24, 2026

## Overview
PriceFuse is developed by Valerii Nikolaev ("we", "us", "the developer").
This Privacy Policy describes how data may be processed when you use the app.
We aim to collect and use as little data as reasonably possible for core functionality.

## Data We Collect
### Data you provide through app features
- Camera and selected photo inputs are processed on your device using Apple Vision to scan prices and recognize text (OCR). The app does not upload these images or recognized amounts to our rates server.
- Optional voice input may capture audio so spoken numbers can be recognized.
- Optional voice recognition may be processed by Apple’s speech services; depending on Apple platform behavior and settings, portions of audio and recognition data may be sent to Apple for processing and service analytics/quality purposes.
- Entered amounts, calculation state, currency selections, and related settings are stored or processed locally on your device. Entered amounts and calculator expressions are not sent to our rates server.
- The paired iPhone and Apple Watch transfer rate data, selected currency information, language settings, Premium access state, and crypto catalog/icon data using Apple WatchConnectivity.

### Rates, crypto assets, icons, and network requests
- The app requests currency rates, crypto quotes, asset catalog information, and crypto icons over HTTPS from our backend hosted on Cloudflare Workers. Our backend obtains reference data from Open Exchange Rates and CoinMarketCap and caches it for delivery to the app.
- Requests can include currency or crypto asset identifiers needed to retrieve quotes or icons. These identifiers describe the requested assets; they do not disclose wallet addresses, private keys, balances, or actual financial transactions. PriceFuse does not provide a wallet or execute cryptocurrency transactions.
- Cloudflare receives IP addresses and other network/request metadata when it handles these requests. It may process and retain network and security data to operate and protect its services under its policies. Our rates application code does not intentionally store client IP addresses in its authentication records or custom log messages, use them to determine your location, or forward them to market-data providers.
- We do not use these requests for advertising or cross-app tracking. Our backend does not maintain a personal conversion history. Upstream market-data requests are made by our server, rather than by forwarding your scanned prices or entered amounts to those providers.

### App authentication and abuse prevention
We use Apple App Attest to help verify requests from a genuine installation of PriceFuse and protect the rates service from abuse. The app sends an App Attest key identifier and cryptographic proof to our backend. The backend stores a hashed installation-related identifier, the associated public key, an Apple attestation receipt, a replay-protection counter, and an expiry time. Short-lived challenge records and session tokens support this verification.

These identifiers allow the service to recognize an app installation for authentication, rate limiting, and security. Hashing does not make an installation identifier anonymous. We do not use it as an advertising identifier or link it to subscription analytics for advertising purposes. Authentication records expire after 90 days without successful registration or authentication; successful authentication renews that period. Expired records are removed by periodic cleanup.

### Operational diagnostics
Our backend records limited operational events, such as authentication operation and result codes, processing duration, and scheduled refresh failures. Cloudflare can retain these custom logs and associated service metadata to help us diagnose failures and maintain the service. Our custom log messages do not include entered amounts, scanned images, voice recordings, raw authentication proofs, or client IP addresses. Cloudflare's network and security processing is separate from these custom log messages.

### Purchases
- If you use subscriptions, purchase and entitlement status is handled through Apple StoreKit.
- We do not receive your full payment card details from Apple.

### What we typically do not collect
- The app does not require user account registration.
- We do not include third-party analytics SDKs or third-party crash-reporting SDKs in the current project build.
- We do not run in-app advertising and we do not sell personal data.

## How We Use Data
We may use data to:
- provide OCR scanning from camera/photos;
- provide voice number recognition;
- provide currency and crypto conversion, refresh reference rates, and deliver asset names and icons;
- authenticate app installations, prevent abuse and replay attacks, and diagnose service failures;
- keep a local cache so conversion can continue to work offline where possible;
- maintain app settings and purchase access state on device.

## Sharing
We may share limited data with service providers only to the extent needed to provide app functionality:
- **Cloudflare**: hosting, delivery and caching of reference rates, catalogs and icons, App Attest verification storage, network security, and operational diagnostics.
- **Market-data providers**: Open Exchange Rates and CoinMarketCap supply reference data and asset information to our backend.
- **Apple services**: StoreKit for purchases, App Attest for authentication, WatchConnectivity between paired devices, and system speech-recognition services when voice input is used.
- **Telegram**: private subscription-event summaries, as described below.

For voice recognition, audio/transcript handling may be performed by Apple according to Apple’s platform behavior and policies. We do not control Apple’s independent data practices.

We do not share personal data with data brokers or sell personal data. Cloudflare describes its network processing in its [Privacy Policy](https://www.cloudflare.com/policies/privacy/).

## Subscription and Purchase Events

Apple sends the developer an App Store Server Notification when there is activity on a purchase or subscription for the app — for example a trial, a renewal, a cancellation, a billing problem, an expiry, or a refund. This is a server-to-server message from Apple; the app itself does not transmit this information from your device.

These notifications describe a purchase or subscription and include pseudonymous transaction information. They contain details such as the product identifier, the price and currency, the App Store storefront country, the app build number, relevant dates, how long a subscription has been active, whether the purchase is Family Shared, and a pseudonymous Apple transaction identifier. They do not contain your name, email address, Apple Account, payment card details, device model, or location.

The developer receives these notifications on a serverless endpoint hosted by Cloudflare, which relays the notification to the developer without an application-level purchase database and forwards a summary to a private Telegram chat with a bot that only the developer can read. The Apple transaction identifier is truncated before it is forwarded, so the message keeps only enough of it to connect events belonging to the same subscription. These records are pseudonymous, rather than guaranteed to be anonymous. This information is used for subscription analytics: how many subscriptions start, renew, or end, and the overall health of the app's paid features. It is never used for advertising, never combined with data from other sources, never sold, and never shared with data brokers.

Cloudflare and Telegram provide the infrastructure used for these summaries and may process data outside your country of residence. We share data with them only for the purposes described here and require the same or equal protection of user data as stated in this Privacy Policy and required by applicable platform rules. Their service terms and privacy policies also describe their processing. We do not use the summaries for advertising or authorize advertising use on our behalf.

We do not normally receive your name or contact details with these notifications or match them to an app account. A transaction reference can nevertheless connect events belonging to a subscription. Contact us if you have a privacy request. We may need sufficient information to locate relevant records and verify your authority; if we cannot identify the relevant records, we will explain that limitation.

We keep subscription summaries only for as long as reasonably needed to monitor paid features and handle related issues. Cancelling a subscription stops future renewal according to Apple's rules; it does not erase previous records or prevent subsequent cancellation, expiry, refund, or other relevant notifications from Apple.

## Data Retention
- Exchange rates, crypto catalogs/icons, calculation state, and app settings are stored locally and may remain until cleared, replaced, or the app is removed. Data already transferred to an Apple Watch is stored separately on that device.
- Backend App Attest registrations follow the 90-day inactivity period described above. Deleting the app does not immediately delete server authentication records.
- Operational logs follow the configured retention of the hosting service. Cloudflare may retain separate network/security data under its own policies; the authentication-record period is not a promise about every provider log.
- We do not retain scanned images or voice recordings on our backend. Voice processing by Apple is governed by Apple's applicable terms and policies.
- Purchase entitlement state may be retained as needed to restore access.

## Security
We use reasonable technical measures and strive to protect data to the extent possible, including HTTPS for rate requests and platform-provided iOS security controls. No method of transmission or storage can be guaranteed to be 100% secure.

## Your Choices
You can typically:
- deny or revoke Camera, Photos, Microphone, and Speech Recognition permissions in iOS Settings;
- stop using voice input and rely on manual input;
- remove local app data by deleting the app;
- manage subscriptions through your Apple Account subscription settings;
- contact us about access, correction, deletion, or other privacy requests, subject to applicable law and our ability to identify the relevant data. Deleting the app or cancelling a subscription does not automatically erase records retained by service providers.

## Children’s Privacy
PriceFuse is not specifically directed to children under 13. We do not knowingly collect personal data from children in a manner inconsistent with applicable law. If you believe a child provided data inappropriately, please contact us.

## International Users
If you use the app outside your home country, data may be processed in other jurisdictions through Apple and service-provider infrastructure. Data-protection laws may differ by region.

## Changes
We may update this Privacy Policy from time to time. We will update the "Last updated" date when changes are made.

## Contact
Developer: Valerii Nikolaev
Contact email: valnikodeveloper@gmail.com
