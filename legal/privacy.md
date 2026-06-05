---
layout: prose
title: Vellichor — Privacy Policy
permalink: /legal/privacy/
lang: en
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
updated: 2026-05-28
redirect_from:
  - /privacy/
---


# Vellichor Privacy Policy

**Effective date**: TBD (date of v1.0 App Store launch)
**Last updated**: 2026-05-28 (draft)

## Introduction

Vellichor is a PDF utility app for Apple platforms (iPhone, iPad, Mac, Apple Watch) built on a single guarantee: **your content is never sent to our servers or any cloud AI — we have none.** Your documents may sync, at your option, only through your own encrypted iCloud (see §3). This Privacy Policy explains what data Vellichor handles, where it lives, and what we do — and do not do — with it.

If you do not agree with this policy, do not use Vellichor. Continued use indicates acceptance.

---

## The short version

- **We don't collect your data.** Vellichor has no servers. All document processing happens on your Apple device.
- **Your PDFs stay in your iCloud.** Document syncing uses your personal iCloud account — Apple's infrastructure, not ours. You can disable iCloud sync per document.
- **Your signatures are encrypted and local.** Stored in your device's Keychain, protected by biometric authentication (Face ID / Touch ID). They never sync, never upload, never leave.
- **AI runs on your device.** Vellichor uses Apple Intelligence (Foundation Models) entirely on-chip. Your document content is not sent to OpenAI, Google, Anthropic, or any cloud service.
- **No advertising. No tracking. No analytics by default.** Optional anonymous usage telemetry can be enabled in Settings (default: off). Disable any time.

---

## 1. Data we do NOT collect

Vellichor does not collect, transmit, or store on our servers:

- The content of your PDF documents
- Your form-fill responses
- Your signatures (drawing data or images)
- Your annotations (highlights, ink, notes)
- Your AI conversation history
- Your scanned documents
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

### 2.1 Signatures

- **What**: Hand-drawn or typed signatures you create within Vellichor
- **Where**: Apple Keychain, encrypted at rest with `kSecAttrAccessibleWhenUnlockedThisDeviceOnly` access policy
- **How protected**: Access requires biometric authentication (Face ID, Touch ID, or device passcode) each session
- **Synced?**: No. Signatures never leave your device. They do not sync via iCloud or any other channel.
- **Why local-only**: Your signature is your most sensitive credential. We will not be the company that loses it in a breach.

### 2.2 Forensic certification metadata

When you sign a PDF with Vellichor's forensic certification enabled:

- **What is embedded in the PDF**:
  - SHA-256 cryptographic hash of the document at the moment of signing (for tamper detection)
  - Apple secure timestamp (when signing occurred)
  - Boolean flag confirming biometric authentication succeeded
  - Approximate device class (e.g., "iPhone 17 Pro Max") — no serial number, no unique identifier
- **What is NOT embedded**:
  - Your IP address
  - Your geolocation
  - Your name, email, or any personal identifier explicitly added by Vellichor
  - Raw biometric data (we receive only a boolean success/failure flag from Apple's biometric system; raw fingerprint or face data never leaves Apple's Secure Enclave)

**Important — what the metadata reveals when you share the PDF**:

When you share the signed PDF, the recipient receives this metadata alongside whatever you've written in the document. If your name appears in the document itself, the metadata becomes associated with you in the recipient's hands. Under GDPR Recital 26, this metadata is considered **pseudonymous** (not fully anonymous) — the device class + timestamp combined with document context could potentially be correlated with you.

**You control this**:
- Toggle "Embed forensic metadata" — default **ON** for tamper detection, but can be disabled per-document
- When disabled, the signature is visual only (drawn signature) without certification metadata
- Forensic metadata cannot be extracted from a flattened PDF (irreversible step before sharing)
- **Where**: Inside your PDF, where you control its distribution
- **Why we do this**: To detect tampering after signing and confirm biometric authentication occurred — without compromising your identity or location

**Important**: Vellichor provides **tamper-evident self-signing** with biometric verification. We make NO eIDAS classification claim — Vellichor is NOT a Qualified Trust Service Provider (QTSP) and the signature is NOT a Qualified Electronic Signature (QES) under eIDAS. Some implementations of our forensic certification may meet criteria for an Advanced Electronic Signature (AES) under eIDAS Art. 26, but we make no certified AES claim. For legally binding signatures under EU law, UK law, US ESIGN Act, or equivalent regulations, use DocuSign, Adobe Sign, or similar certified providers.

### 2.3 Biometric authentication

- We never see, store, or transmit your biometric data (fingerprint, face)
- Apple's Secure Enclave handles all biometric processing
- Vellichor receives only a success/failure result from `LocalAuthentication.framework`
- If you disable biometrics in iOS Settings, Vellichor falls back to your device passcode

---

## 3. Data that syncs via your iCloud

You control whether your documents sync across your Apple devices via iCloud. When sync is enabled:

### 3.1 What syncs

- PDF documents themselves: stored in **your iCloud Drive** (your iCloud account, your storage quota)
- Document metadata (titles, import date, last opened): syncs via **CloudKit Private Database** to container `iCloud.com.khassinx.vellichor`
- Annotations (highlights, ink, notes): CloudKit Private Database
- Form-fill state: CloudKit Private Database (note: form values become embedded in the PDF itself once saved)
- AI conversation history per document: CloudKit Private Database
- Scanner output metadata + OCR text: CloudKit Private Database

### 3.2 What does NOT sync

- Signatures (Keychain-local only)
- Documents you mark "Local only" via per-document toggle
- Onboarding state and app preferences (UserDefaults, local only)
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
- Text is chunked, embedded, and indexed entirely on-device using Apple's Foundation Models
- Your query is processed on-device by Apple's language model
- Responses are generated on-device with citations to specific pages
- **No document content, queries, or responses are sent to our servers or any third-party AI service** — all AI processing is on-device
- **Nothing is sent to OpenAI, Anthropic, Google, or any third-party AI service**

### Device requirements

- iPhone 15 Pro / Pro Max, iPhone 16/17 series, or newer (Apple Intelligence-eligible devices)
- iPad with Apple Intelligence support (M-series chips and selected A-series)
- Apple Silicon Mac (M1 or later) — Intel Macs are not supported for AI features
- Apple Watch: AI features unavailable on Watch directly; voice queries are forwarded to your paired iPhone via WatchConnectivity for processing

On devices that don't support Apple Intelligence, AI features are gracefully disabled with a clear message. We do not paywall or fake AI features on unsupported devices.

---

## 5. Forms and form-fill data

When you fill an interactive PDF form (AcroForm) using Vellichor:

- Your responses are stored as standard PDF annotation widgets — **inside your PDF**, not in any separate database
- The PDF remains your file; we have no copy
- If you sync the PDF via iCloud, form-fill state syncs along with the PDF (your iCloud, not ours)
- You can flatten the form to make field values permanent (irreversible) before sharing

---

## 6. Scanner and OCR

When you use Vellichor's document scanner:

- Camera capture is handled by Apple's `VNDocumentCameraViewController` (Apple-native scanner)
- Image processing (edge detection, perspective correction) happens on-device
- OCR text recognition uses Apple's `Vision` framework (`RecognizeDocumentsRequest`) on-device
- Generated PDF is saved to your library and stays on-device unless you choose to share or sync

Camera, Photos, and microphone permissions are requested per Apple's standard permission flow. You can revoke any time in iOS Settings.

---

## 7. Optional anonymous telemetry (v1.1+)

In a future version (v1.1+), Vellichor may offer optional anonymous usage telemetry powered by **TelemetryDeck** (a privacy-first analytics service).

**If we enable this feature**, it will be:

- **Disabled by default** — you opt in explicitly via Settings
- **Anonymous** — no user identifiers, no IP addresses, no PII
- **Aggregated** — only feature usage counts (e.g., "scan used 12 times" — never "user X scanned document Y")
- **Documented** — exact data points listed in this Privacy Policy upon launch
- **Revocable** — disable anytime in Settings

Until v1.1 ships with this opt-in feature documented here, Vellichor performs **zero analytics**.

---

## 8. Children and family use

- Vellichor is rated 4+ on the App Store. The app does not contain age-inappropriate content.
- Vellichor does not knowingly collect personal data from any user, including children.
- We comply with COPPA principles by not collecting any personal data via the app.
- Parents using Family Sharing may share Vellichor with children's accounts; standard Apple parental controls apply.
- If a parent or guardian believes Vellichor has inadvertently received personal data from a child, contact us (see §13) — though we note again that the app architecture makes this categorically not possible.

---

## 9. App Store and payment processing

- All purchases (Pro Unlock IAP, $24.99 one-time) are processed by Apple via the App Store
- Apple receives your payment information; Vellichor never sees it
- Apple receives the purchase receipt; Vellichor verifies receipts on-device using `StoreKit 2`
- Restore Purchases works via Apple's standard receipt mechanism (no network calls to our servers, because we have none)
- Refund requests are handled by Apple per their standard refund policy

---

## 10. Data we may receive from Apple

Apple may share aggregated, anonymized App Store metrics with us (downloads, retention rates, etc.) via App Store Connect. This data:

- Cannot be tied to individual users
- Is provided by Apple, not collected by us
- Helps us understand product-market fit and improve features

---

## 11. Third-party services

Vellichor does NOT integrate with:

- Cloud storage services (Dropbox, Google Drive, Box, OneDrive)
- Cloud AI services (OpenAI, Anthropic, Google, Microsoft, Meta)
- Analytics platforms (Google Analytics, Mixpanel, Amplitude, Adjust)
- Advertising networks (anywhere)
- Social media integrations (Facebook SDK, Twitter SDK, etc.)
- Crash reporting services beyond Apple's native (Apple Crash Reporting handles this)

Your data goes nowhere except where you explicitly send it (e.g., the Share Sheet to email a PDF you control).

---

## 12. Your rights

You can:

- **Access your data**: it's already on your device — open Vellichor and view everything
- **Export your data**: use Vellichor's Export feature to take everything elsewhere in standard formats (PDF, JPG, Markdown, JSON, CSV)
- **Delete your data**: delete documents in-app, or uninstall Vellichor — all locally stored data is removed (signatures in Keychain are removed on uninstall; iCloud data follows Apple's standard retention)
- **Revoke iCloud access**: iOS Settings → iCloud → Vellichor → off
- **Revoke biometric access**: iOS Settings → Face ID & Passcode → app permissions
- **Disable analytics**: when telemetry exists (v1.1+), Settings → Privacy → Analytics → off
- **Request information**: contact us (see §13) — though we will likely respond "we don't have it" because we don't

Under GDPR (EU), CCPA (California), LGPD (Brazil), and similar jurisdictional rights:
- Right to access: see above
- Right to rectification: edit on-device anytime
- Right to erasure: uninstall removes local data; iCloud follows Apple's policy
- Right to data portability: Export feature
- Right to object to processing: turn off Vellichor — there's nothing to object to
- Right to lodge a complaint: contact your local data protection authority

---

## 13. Contact + EU representative

For privacy questions:

- **Email**: hello@khassinx.com
- **Response target**: within 7 business days
- **For security disclosures**: see vellichor.khassinx.com/security (security.txt file)

### EU representative (GDPR Article 27)

KHASSINX LLC (a Florida limited liability company), the operator of Vellichor and a non-EU controller offering services to EU users, makes the following declaration:

Vellichor's architecture is **zero-collection on Vellichor's side** — no personal data is transmitted to KhassinX servers (because there are no KhassinX servers). The on-device hash + timestamp + biometric boolean + approximate device class processed during forensic certification is processed exclusively on the user's Apple device, never reaches KhassinX systems, and falls outside the territorial scope clarifications of GDPR Art. 3(2) for "processing" by the controller.

**However**, to maximize defensibility and respect EU users' rights:
- We are evaluating designation of an EU representative per Art. 27. Pending designation, this section serves as transparent disclosure.
- EU users may exercise their GDPR rights by contacting `hello@khassinx.com`.
- A formal EU representative will be designated before any feature is added that would qualify as KhassinX-side processing (e.g., optional TelemetryDeck v1.1).

### Data Protection Officer / Brazilian Encarregado (LGPD)

- **DPO / Encarregado**: KhassinX Privacy Office
- **Contact**: hello@khassinx.com
- **LGPD rights** (Art. 18): access, correction, deletion, portability, anonymization, objection — exercisable via the contact above.

---

## 14. Changes to this policy

We will update this policy when:

- New features change what data is handled
- Optional telemetry is added (v1.1)
- Legal requirements change

When we update, we'll:

- Update the "Last updated" date at top
- Notify users in-app on next launch when changes are material
- Maintain previous versions at `vellichor.khassinx.com/privacy/archive/`

---

## 15. Standards alignment

Vellichor's privacy practices align with:

- **GDPR** (EU Regulation 2016/679) — Articles 5 (principles), 25 (privacy by design), 32 (security)
- **CCPA** (California Civil Code §1798.100 et seq.) — no sale of personal information (we collect none)
- **LGPD** (Brazil Federal Law 13.709/2018) — lawful basis: legitimate interest (utility provision); minimal data principle
- **PIPEDA** (Canada) — consent and minimal collection principles
- **eIDAS** (EU Regulation 910/2014) — note: Vellichor signatures are Simple Electronic Signatures (SES), not Advanced (AES) or Qualified (QES). See §2.2.
- **ISO/IEC 27001 principles** — information security alignment (not certified)

This policy does NOT constitute legal advice. For jurisdiction-specific advice, consult a qualified attorney.

---

*Vellichor is built by KhassinX. We respect your privacy because you trusted us with your documents. Thank you.*
