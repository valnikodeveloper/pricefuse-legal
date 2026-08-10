# Privacy Policy for PriceFuse

Last updated: August 9, 2026

## Overview
PriceFuse is developed by Valerii Nikolaev ("we", "us", "the developer").
This Privacy Policy describes how data may be processed when you use the app.
We aim to collect and use as little data as reasonably possible for core functionality.

## Data We Collect
### Data you provide through app features
- Camera and photo library inputs may be used so the app can scan prices and recognize text (OCR).
- Optional voice input may capture audio so spoken numbers can be recognized.
- Optional voice recognition may be processed by Apple’s speech services; depending on Apple platform behavior and settings, portions of audio and recognition data may be sent to Apple for processing and service analytics/quality purposes.
- Currency selections and related app settings may be stored locally on your device.

### Data processed by app infrastructure
- Currency rates are fetched from an external rates provider over HTTPS.
- Requests to external services may include technical network metadata (for example, IP address and standard request metadata) as part of normal internet communication.

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
- provide currency conversion and refresh exchange rates;
- keep a local cache so conversion can continue to work offline where possible;
- maintain app settings and purchase access state on device.

## Sharing
We may share limited data with service providers only to the extent needed to provide app functionality:
- **Exchange rate provider**: requests for currency rates over HTTPS.
- **Apple services**: StoreKit for purchases and Apple system speech-recognition services when voice input is used.

For voice recognition, audio/transcript handling may be performed by Apple according to Apple’s platform behavior and policies. We do not control Apple’s independent data practices.

Other than the above, we do not intentionally share personal data with data brokers, and we do not sell personal data.

## Subscription and Purchase Events

Apple sends the developer an App Store Server Notification when there is activity on a purchase or subscription for the app — for example a trial, a renewal, a cancellation, a billing problem, an expiry, or a refund. This is a server-to-server message from Apple; the app itself does not transmit this information from your device.

These notifications describe the transaction, not your identity. They contain details such as the product identifier, the price and currency, the App Store storefront country, the app build number, relevant dates, how long a subscription has been active, whether the purchase is Family Shared, and a pseudonymous Apple transaction identifier. They do not contain your name, email address, Apple Account, payment card details, device model, or location.

The developer receives these notifications on a serverless endpoint hosted by Cloudflare, which processes them in transit without storing them, and forwards a summary to a private Telegram chat with a bot that only the developer can read. The Apple transaction identifier is truncated before it is forwarded, so the message keeps only enough of it to connect events belonging to the same subscription. This information is used solely for the developer's own purposes, primarily analytics: how many subscriptions start, renew, or end, and the overall health of the app's paid features. It is never used for advertising, never combined with data from other sources, never sold, and never shared with data brokers.

Cloudflare and Telegram act as service providers for this data and may process it outside your country of residence. We share it with them only to the extent described above, and we require that they provide the same or equal protection of user data as set out in this Privacy Policy. We do not authorize them to use it for their own purposes.

These messages are not linked to an account, an email address, or any identifier you could give us. We deliberately do not collect anything that would let us connect them to you — which also means we are not able to locate your records if you ask us to. We will not delete records on the basis of an unverified description, because responding to such a request would itself confirm to whoever asked that a matching purchase exists. Where a controller cannot identify a data subject, data protection law does not require it to collect additional information for the sole purpose of enabling such requests.

We keep these messages only for as long as they are useful for monitoring the app's paid features. Cancelling your subscription in your Apple Account settings stops any further events from being generated.

## Data Retention
- Exchange-rate cache and app settings are typically stored locally and may remain until cleared, overwritten, or the app is removed.
- OCR and voice inputs are typically processed for immediate app functionality; we strive not to retain raw media longer than needed for that purpose.
- Purchase entitlement state may be retained as needed to restore access.

## Security
We use reasonable technical measures and strive to protect data to the extent possible, including HTTPS for rate requests and platform-provided iOS security controls. No method of transmission or storage can be guaranteed to be 100% secure.

## Your Choices
You can typically:
- deny or revoke Camera, Photos, Microphone, and Speech Recognition permissions in iOS Settings;
- stop using voice input and rely on manual input;
- remove local app data by deleting the app;
- manage subscriptions through your Apple ID subscription settings.

## Children’s Privacy
PriceFuse is not specifically directed to children under 13. We do not knowingly collect personal data from children in a manner inconsistent with applicable law. If you believe a child provided data inappropriately, please contact us.

## International Users
If you use the app outside your home country, data may be processed in other jurisdictions through Apple and service-provider infrastructure. Data-protection laws may differ by region.

## Changes
We may update this Privacy Policy from time to time. We will update the "Last updated" date when changes are made.

## Contact
Developer: Valerii Nikolaev
Contact email: valnikodeveloper@gmail.com
