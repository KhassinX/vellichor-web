---
layout: prose
title: Vellichor — Privacy Policy
permalink: /legal/privacy/
lang: en
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
updated: 2026-06-28
redirect_from:
  - /privacy/
---


# Vellichor Privacy Policy

**Effective date**: TBD (date of v1.0 App Store launch)
**Last updated**: 2026-06-28 (draft — scope aligned to v1.0: a PDF Q&A reader)

## Introduction

Vellichor is a PDF reading and question-answering app for Apple platforms (iPhone, iPad, and Mac) built on a single design principle: **your content is never sent to our servers or any cloud AI — we have none.** Your documents may sync, at your option, only through your own encrypted iCloud (see §3). This Privacy Policy explains what data Vellichor handles, where it lives, and what we do — and do not do — with it.

If you do not agree with this policy, do not use Vellichor. Continued use indicates acceptance.

---

## The short version

- **We don't collect your data.** Vellichor has no servers. All document processing happens on your Apple device.
- **Your PDFs stay in your iCloud.** Document syncing uses your personal iCloud account — Apple's infrastructure, not ours. You can disable iCloud sync per document.
- **AI runs on your device.** Vellichor uses Apple Intelligence (Foundation Models) entirely on-chip. Your document content is not sent to OpenAI, Google, Anthropic, or any cloud service.
- **No advertising. No tracking. No third-party analytics.** Vellichor includes no advertising, tracking, or third-party analytics SDKs — none. App diagnostics use Apple's on-device MetricKit and never leave your device.

---

## 1. Data we do NOT collect

Vellichor does not collect, transmit, or store on our servers:

- The content of your PDF documents
- Your annotations (highlights, notes)
- Your AI conversation history
- Your IP address
- Your geolocation
- Your device serial number or persistent identifiers
- Your name, email, or contact information (beyond Apple ID required for App Store purchase, handled entirely by Apple)
- Behavioral analytics tied to your identity
- Cookies or web tracking pixels

We don't collect this because we don't have servers. There is nowhere for it to go.

---

## 2. Data that stays on your device

These categories of data are stored exclusively on your Apple device:

### 2.1 App preferences and reading settings

- **What**: onboarding state and reading preferences (page appearance theme, library sort order, per-document "Local only" choices)
- **Where**: stored locally on your device via `UserDefaults`
- **Synced?**: app preferences and onboarding state are local to each device and do not sync
- **Why local-only**: these are device conveniences; there is nothing sensitive to put anywhere else

### 2.2 On-device search index

- **What**: to answer questions about a PDF and to power search, Vellichor extracts the document's text with `PDFKit` and builds a semantic index (text chunks and embeddings) on your device
- **Where**: inside Vellichor's app container on your device
- **Synced?**: the index is derived data, rebuilt on-device as needed; it is never uploaded to us
- **Why local-only**: this index is what makes on-device Q&A and search possible without sending your document anywhere

### 2.3 On-device diagnostics

- **What**: Vellichor uses Apple's `MetricKit` to gather on-device stability and performance diagnostics (e.g., hangs, crashes, disk and memory metrics)
- **Where**: stored locally under the app's `Caches` directory, automatically rotated and deleted after at most 30 days
- **Synced?**: No. These diagnostics never leave your device, are never uploaded to us, and are not sent over any network by Vellichor
- **Why local-only**: we improve quality using Apple's privacy-preserving, on-device tooling instead of third-party crash or analytics SDKs (we use none)

---

## 3. Data that syncs via your iCloud

You control whether your documents sync across your Apple devices via iCloud. When sync is enabled:

### 3.1 What syncs

- PDF documents themselves: stored in **your iCloud Drive** (your iCloud account, your storage quota)
- Document metadata (titles, import date, last opened): syncs via **CloudKit Private Database** to container `iCloud.com.khassinx.vellichor`
- Annotations (highlights, notes): CloudKit Private Database
- AI conversation history per document: CloudKit Private Database

### 3.2 What does NOT sync

- Documents you mark "Local only" via per-document toggle
- Onboarding state and app preferences (UserDefaults, local only)
- On-device diagnostics (MetricKit, local only)
- AI conversation history if you disable conversation sync

### 3.3 iCloud responsibility

- iCloud is Apple's infrastructure, not ours
- Apple is the data controller for content stored in iCloud per Apple's Privacy Policy
- We have no access to your iCloud data; we only request CloudKit Private Database access (per-user, isolated)
- You can revoke Vellichor's iCloud access anytime in iOS Settings → [your name] → iCloud → Vellichor

### 3.4 Family Sharing

If you share Vellichor via Family Sharing:

- Each family member's documents remain in **their own** iCloud account
- No document content is shared with other family members through Vellichor
- The Pro Unlock is shared (per Apple Family Sharing rules), but individual privacy remains per-account

---

## 4. AI Q&A and Apple Intelligence

Vellichor uses Apple Intelligence (Foundation Models framework) for on-device question answering, semantic search, and document summarization.

### How Foundation Models works in Vellichor

- Document text is extracted using `PDFKit` on your device
- Text is chunked, embedded, and indexed entirely on-device
- Your query is processed on-device by Apple's language model
- Responses are generated on-device with citations to specific pages
- **No document content, queries, or responses are sent to our servers or any third-party AI service** — all AI processing is on-device
- **Nothing is sent to OpenAI, Anthropic, Google, or any third-party AI service**

### Device requirements

- iPhone 15 Pro / Pro Max, iPhone 16/17 series, or newer (Apple Intelligence-eligible devices)
- iPad with Apple Intelligence support (M-series chips and selected A-series)
- Apple Silicon Mac (M1 or later) — Intel Macs are not supported for AI features

On devices that don't support Apple Intelligence, AI features are gracefully disabled with a clear message. We do not paywall or fake AI features on unsupported devices.

---

## 5. Children and family use

- Vellichor is rated 4+ on the App Store. The app does not contain age-inappropriate content.
- Vellichor does not knowingly collect personal data from any user, including children.
- We comply with COPPA principles by not collecting any personal data via the app.
- Parents using Family Sharing may share Vellichor with children's accounts; standard Apple parental controls apply.
- If a parent or guardian believes Vellichor has inadvertently received personal data from a child, contact us (see §10) — though we note again that the app architecture makes this categorically not possible.

---

## 6. App Store and payment processing

- All purchases (Pro Unlock IAP, $14.99 one-time) are processed by Apple via the App Store
- Apple receives your payment information; Vellichor never sees it
- Apple receives the purchase receipt; Vellichor verifies receipts on-device using `StoreKit 2`
- Restore Purchases works via Apple's standard receipt mechanism (no network calls to our servers, because we have none)
- Refund requests are handled by Apple per their standard refund policy

---

## 7. Data we may receive from Apple

Apple may share aggregated, anonymized App Store metrics with us (downloads, retention rates, etc.) via App Store Connect. This data:

- Cannot be tied to individual users
- Is provided by Apple, not collected by us
- Helps us understand product-market fit and improve features

---

## 8. Third-party services

Vellichor does NOT integrate with:

- Cloud storage services (Dropbox, Google Drive, Box, OneDrive)
- Cloud AI services (OpenAI, Anthropic, Google, Microsoft, Meta)
- Analytics platforms (Google Analytics, Mixpanel, Amplitude, Adjust)
- Advertising networks (anywhere)
- Social media integrations (Facebook SDK, Twitter SDK, etc.)
- Crash or analytics reporting services beyond Apple's native, on-device tooling (Vellichor uses Apple's `MetricKit` on-device only)

Your data goes nowhere except where you explicitly send it (e.g., the Share Sheet to email a PDF you control).

---

## 9. Your rights

For the full set of rights you have under GDPR (EU/EEA), the UK GDPR, Spain's LOPDGDD, California's CCPA/CPRA, other US states, and elsewhere — and the channels to exercise them — see KhassinX's **[Privacy Rights Center](https://khassinx.com/legal/your-rights/)**. The rights are the same across every KhassinX app, so we maintain them in one place rather than duplicating them here.

In Vellichor specifically, you can exercise them directly — most without contacting anyone, because the data is already yours:

- **Access your data**: it's already on your device — open Vellichor and view everything
- **Export your data**: your PDFs are already standard files you can share anywhere; Vellichor can also export your AI conversations to Markdown
- **Delete your data**: delete documents in-app, or uninstall Vellichor — all locally stored data is removed; iCloud data follows Apple's standard retention, and you can delete it from your Apple ID at any time
- **Revoke iCloud access**: iOS Settings → iCloud → Vellichor → off

To make a formal request or lodge a question, email [`legal@khassinx.com`](mailto:legal@khassinx.com) — though we will likely respond "we don't have it," because we don't.

---

## 10. Contact + EU representative

For privacy questions:

- **Email**: [legal@khassinx.com](mailto:legal@khassinx.com)
- **Response target**: within 7 business days
- **For security disclosures**: see vellichor.khassinx.com/security (security.txt file)

### EU representative (GDPR Article 27)

KHASSINX LLC (a Florida limited liability company), the operator of Vellichor and a non-EU controller offering services to EU users, makes the following declaration:

Vellichor's architecture is **zero-collection on Vellichor's side** — no personal data is transmitted to KhassinX servers (because there are no KhassinX servers). All document processing, AI Q&A, search indexing, and diagnostics occur exclusively on the user's Apple device, never reach KhassinX systems, and fall outside the territorial scope clarifications of GDPR Art. 3(2) for "processing" by the controller.

**However**, to maximize defensibility and respect EU users' rights:
- We are evaluating designation of an EU representative per Art. 27. Pending designation, this section serves as transparent disclosure.
- EU users may exercise their GDPR rights by contacting [`legal@khassinx.com`](mailto:legal@khassinx.com), or via the [Privacy Rights Center](https://khassinx.com/legal/your-rights/).
- A formal EU representative will be designated before any feature is added that would qualify as KhassinX-side processing of personal data.

### Data Protection Officer / Brazilian Encarregado (LGPD)

- **DPO / Encarregado**: KhassinX Privacy Office
- **Contact**: [legal@khassinx.com](mailto:legal@khassinx.com)
- **LGPD rights** (Art. 18): access, correction, deletion, portability, anonymization, objection — exercisable via the contact above.

---

## 11. Changes to this policy

We will update this policy when:

- New features change what data is handled
- Legal requirements change

When we update, we'll:

- Update the "Last updated" date at top
- Notify users in-app on next launch when changes are material
- Maintain previous versions at `vellichor.khassinx.com/privacy/archive/`

---

## 12. Standards alignment

Vellichor's privacy practices align with:

- **GDPR** (EU Regulation 2016/679) — Articles 5 (principles), 25 (privacy by design), 32 (security)
- **CCPA** (California Civil Code §1798.100 et seq.) — no sale of personal information (we collect none)
- **LGPD** (Brazil Federal Law 13.709/2018) — lawful basis: legitimate interest (utility provision); minimal data principle
- **PIPEDA** (Canada) — consent and minimal collection principles
- **ISO/IEC 27001 principles** — information security alignment (not certified)

This policy does NOT constitute legal advice. For jurisdiction-specific advice, consult a qualified attorney.

---

*Vellichor is built by KhassinX. We respect your privacy because you trusted us with your documents. Thank you.*
