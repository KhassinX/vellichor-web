---
layout: prose
title: Vellichor — Privacy Policy
permalink: /legal/privacy/
lang: en
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
canonical_pt-BR: /pt-BR/legal/privacy/
canonical_de: /de/legal/privacy/
updated: 2026-05-27
redirect_from:
  - /privacy/
---

# Privacy Policy

**Effective date: 2026-05-27**

This is the privacy policy for **Vellichor**, a PDF Q&A app for Apple platforms built by **KhassinX**.

We wrote this in plain language because we want you to actually read it.

## The short version

- **We do not collect, store, or transmit your PDFs or your queries about them.** Vellichor runs Apple Intelligence Foundation Models on your device.
- **We have no analytics, no tracking SDKs, no third-party services in v1.** Not Firebase, not Google Analytics, not Mixpanel, not Sentry, not Crashlytics. None.
- **We have no account system.** There is nothing to sign up for, no email to give us, no password to forget.
- **Your library and annotations sync between your devices via your own iCloud.** Apple encrypts this end-to-end; we never see it.
- **Your purchase is verified by Apple, not by us.** We do not store payment information or know what you paid.

## What data Vellichor handles

### Documents (your PDFs)

Vellichor reads the PDFs you import from Files, Share Sheet, camera scans, drag-and-drop, or iCloud Drive. These documents are stored:

- **On your device**, in Vellichor's application container
- **In your personal iCloud Drive** under the Vellichor app folder, if you enable iCloud sync (so the same documents appear on your other Apple devices)

We — KhassinX — have no access to these documents at any point. They never reach a server we control. They never reach Apple's servers in a form Apple can read either; iCloud Drive uses end-to-end encryption tied to your Apple ID.

### Questions you ask and answers Vellichor generates

When you ask Vellichor a question about a PDF, the question is processed by Apple Intelligence Foundation Models running locally on your iPhone, iPad, or Mac. The model produces an answer using the document content as context.

- **The question never leaves your device.**
- **The answer never leaves your device.**
- The conversation history is stored on your device (and synced via your personal iCloud across your devices, if iCloud is enabled).

### Annotations, highlights, and notes

Anything you mark up — text highlights, typed notes, Apple Pencil handwriting — is stored in CloudKit's private database under your Apple ID. CloudKit private database is end-to-end encrypted; only your devices can read it. We cannot.

### Subscription / purchase state

Vellichor uses **StoreKit 2** (Apple's in-app purchase system) for the one-time Pro unlock. When you purchase, Apple confirms the transaction directly with your device's App Store. We do not run a payment server, do not store credit-card information, and do not know your real name, email, or billing address. We can see, via Apple's anonymous receipt validation, only whether a given install has purchased Pro — nothing more.

Family Sharing is supported: if a family member has purchased Vellichor Pro, your device receives the entitlement automatically through Apple.

### Crash reports and diagnostics

If Vellichor crashes, Apple's standard crash reporting may include an anonymous report sent to Apple **if and only if you have opted in via iOS Settings → Privacy & Security → Analytics & Improvements → Share with App Developers**. This is Apple's mechanism, not ours. We receive aggregated, fully anonymous crash logs through App Store Connect; they do not contain document content, questions, answers, or any personally identifiable information.

If you have not opted in to Apple's analytics sharing, we receive nothing.

## What data Vellichor does NOT handle

- **No analytics SDKs.** No Firebase Analytics, Google Analytics, Mixpanel, Amplitude, Segment, Sentry, Crashlytics, AppsFlyer, Adjust, Branch, Singular, Kochava, Apphud, RevenueCat, or any other third-party telemetry tool. None.
- **No advertising.** No ad networks, no tracking pixels, no IDFA collection, no SKAdNetwork attribution.
- **No social logins.** No "Sign in with Google", no Facebook SDK, no third-party identity provider.
- **No external AI.** Vellichor only uses Apple Intelligence on-device. We do not send your content to OpenAI, Anthropic, Google, or any other AI provider in v1.

## Children

Vellichor is rated 4+ and contains no objectionable content. We do not knowingly collect any data from children because **we do not collect any data from anyone**.

## Your rights

Because we collect no data, there is nothing for us to access, correct, delete, or export at your request. You may, of course, delete the app and (separately) remove its iCloud data from your Apple ID at any time.

If you live in a jurisdiction with specific privacy rights (GDPR in the EU/UK, CCPA in California, LGPD in Brazil, and others), those rights still apply, but their practical effect on Vellichor is minimal: we are not the data controller of anything about you.

## Changes to this policy

If we ever change this policy, we will update the "Effective date" at the top and publish the new version at this URL. The previous version will remain accessible via the GitHub commit history of this site ([khassinx/vellichor-www](https://github.com/khassinx/vellichor-www)).

We will not retroactively expand what data we collect. If a future Vellichor feature requires any collection (for example, an optional bug-reporting opt-in), it will be opt-in and explicit, and this policy will be updated before such a feature ships.

## Contact

- **Privacy questions**: [hello@khassinx.com](mailto:hello@khassinx.com)
- **Security disclosure**: [security@khassinx.com](mailto:security@khassinx.com) ([policy](/security/))
- **Developer**: KhassinX
