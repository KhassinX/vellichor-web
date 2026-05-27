---
layout: prose
title: Vellichor — Datenschutzerklärung
permalink: /de/legal/privacy/
lang: de
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
canonical_pt-BR: /pt-BR/legal/privacy/
canonical_de: /de/legal/privacy/
updated: 2026-05-27
---

# Datenschutzerklärung

**Wirksam ab: 2026-05-27**

Dies ist die Datenschutzerklärung für **Vellichor**, eine PDF-Q&A-App für Apple-Plattformen, entwickelt von **KhassinX**.

Wir haben dies in klarer Sprache geschrieben, damit Sie es tatsächlich lesen.

## Kurzfassung

- **Wir erfassen, speichern oder übertragen weder Ihre PDFs noch Ihre Anfragen dazu.** Vellichor führt Apple Intelligence Foundation Models auf Ihrem Gerät aus.
- **Keine Analytics, keine Tracking-SDKs, keine Drittanbieter-Dienste in v1.** Kein Firebase, kein Google Analytics, kein Mixpanel, kein Sentry, kein Crashlytics. Keine.
- **Es gibt kein Kontosystem.** Sie müssen sich nicht registrieren, geben uns keine E-Mail-Adresse und haben kein Passwort, das Sie vergessen könnten.
- **Ihre Bibliothek und Anmerkungen synchronisieren zwischen Ihren Geräten über Ihr eigenes iCloud.** Apple verschlüsselt das Ende-zu-Ende; wir sehen es nie.
- **Ihren Kauf verifiziert Apple, nicht wir.** Wir speichern keine Zahlungsinformationen und wissen nicht, wie viel Sie bezahlt haben.

## Welche Daten Vellichor verarbeitet

### Dokumente (Ihre PDFs)

Vellichor liest die PDFs, die Sie aus der Dateien-App, dem Teilen-Menü, Kamerascans, Drag-and-Drop oder iCloud Drive importieren. Diese Dokumente werden gespeichert:

- **Auf Ihrem Gerät**, im Anwendungs-Container von Vellichor
- **In Ihrem persönlichen iCloud Drive** im Vellichor-Ordner, wenn Sie iCloud-Sync aktivieren (damit dieselben Dokumente auf Ihren anderen Apple-Geräten erscheinen)

Wir — KhassinX — haben zu keinem Zeitpunkt Zugriff auf diese Dokumente. Sie erreichen nie einen Server, den wir kontrollieren. Sie erreichen auch nicht die Apple-Server in einer für Apple lesbaren Form; iCloud Drive verwendet Ende-zu-Ende-Verschlüsselung, die an Ihre Apple-ID gebunden ist.

### Fragen, die Sie stellen, und Antworten, die Vellichor generiert

Wenn Sie Vellichor eine Frage zu einem PDF stellen, wird die Frage von Apple Intelligence Foundation Models verarbeitet, die lokal auf Ihrem iPhone, iPad oder Mac laufen. Das Modell erzeugt eine Antwort unter Verwendung des Dokumentinhalts als Kontext.

- **Die Frage verlässt Ihr Gerät nie.**
- **Die Antwort verlässt Ihr Gerät nie.**
- Der Konversationsverlauf wird auf Ihrem Gerät gespeichert (und synchronisiert über Ihr persönliches iCloud zwischen Ihren Geräten, falls iCloud aktiviert ist).

### Anmerkungen, Hervorhebungen und Notizen

Alles, was Sie markieren — Texthervorhebungen, getippte Notizen, Apple-Pencil-Handschrift — wird in der privaten CloudKit-Datenbank unter Ihrer Apple-ID gespeichert. Die private CloudKit-Datenbank ist Ende-zu-Ende-verschlüsselt; nur Ihre Geräte können sie lesen. Wir nicht.

### Abonnement-/Kaufstatus

Vellichor nutzt **StoreKit 2** (Apples In-App-Kaufsystem) für die einmalige Pro-Freischaltung. Wenn Sie kaufen, bestätigt Apple die Transaktion direkt mit dem App Store Ihres Geräts. Wir betreiben keinen Zahlungsserver, speichern keine Kreditkartendaten und kennen weder Ihren echten Namen noch Ihre E-Mail-Adresse oder Rechnungsanschrift. Über Apples anonyme Belegvalidierung können wir lediglich erkennen, ob eine bestimmte Installation Pro gekauft hat — mehr nicht.

Family Sharing wird unterstützt: Wenn ein Familienmitglied Vellichor Pro gekauft hat, erhält Ihr Gerät die Berechtigung automatisch über Apple.

### Absturzberichte und Diagnose

Wenn Vellichor abstürzt, kann Apples Standard-Absturzberichtssystem einen anonymen Bericht an Apple senden — **nur dann, wenn Sie in iOS-Einstellungen → Datenschutz & Sicherheit → Analyse & Verbesserungen → Mit App-Entwicklern teilen zugestimmt haben**. Das ist Apples Mechanismus, nicht unserer. Wir erhalten aggregierte, vollständig anonyme Crash-Logs über App Store Connect; diese enthalten keinen Dokumentinhalt, keine Fragen, keine Antworten und keine personenbezogenen Daten.

Wenn Sie Apples Analytics-Teilen nicht aktiviert haben, erhalten wir nichts.

## Welche Daten Vellichor NICHT verarbeitet

- **Keine Analytics-SDKs.** Kein Firebase Analytics, Google Analytics, Mixpanel, Amplitude, Segment, Sentry, Crashlytics, AppsFlyer, Adjust, Branch, Singular, Kochava, Apphud, RevenueCat oder ein anderes Drittanbieter-Telemetrie-Tool. Keine.
- **Keine Werbung.** Keine Werbenetzwerke, keine Tracking-Pixel, keine IDFA-Erfassung, keine SKAdNetwork-Attribution.
- **Keine Social Logins.** Kein „Mit Google anmelden", kein Facebook-SDK, kein Drittanbieter-Identitätsanbieter.
- **Keine externe KI.** Vellichor verwendet ausschließlich Apple Intelligence auf dem Gerät. Wir senden Ihren Inhalt in v1 nicht an OpenAI, Anthropic, Google oder einen anderen KI-Anbieter.

## Kinder

Vellichor ist mit 4+ bewertet und enthält keine anstößigen Inhalte. Wir erfassen wissentlich keine Daten von Kindern, weil **wir von niemandem Daten erfassen**.

## Ihre Rechte

Da wir keine Daten erfassen, gibt es nichts, worauf wir auf Ihr Verlangen hin zugreifen, das wir korrigieren, löschen oder exportieren könnten. Sie können die App selbstverständlich jederzeit löschen und (gesondert) ihre iCloud-Daten aus Ihrer Apple-ID entfernen.

Falls Sie in einer Rechtsordnung mit spezifischen Datenschutzrechten leben (DSGVO in der EU/im UK, CCPA in Kalifornien, LGPD in Brasilien und andere), gelten diese Rechte weiterhin, aber ihre praktische Auswirkung auf Vellichor ist minimal: Wir sind nicht der Datenverantwortliche für irgendetwas über Sie.

## Änderungen dieser Erklärung

Sollten wir diese Erklärung jemals ändern, aktualisieren wir das „Wirksam ab"-Datum oben und veröffentlichen die neue Version unter dieser URL. Die vorherige Version bleibt über die GitHub-Commit-Historie dieser Website zugänglich ([khassinx/vellichor-www](https://github.com/khassinx/vellichor-www)).

Wir werden nicht rückwirkend ausweiten, welche Daten wir erfassen. Falls eine zukünftige Vellichor-Funktion irgendeine Erfassung erfordert (zum Beispiel ein optionales Bug-Reporting-Opt-In), wird sie opt-in und explizit sein, und diese Erklärung wird aktualisiert, bevor eine solche Funktion ausgeliefert wird.

## Kontakt

- **Datenschutzanfragen**: [hello@khassinx.com](mailto:hello@khassinx.com)
- **Sicherheits-Meldungen**: [security@khassinx.com](mailto:security@khassinx.com) ([Richtlinie](/de/security/))
- **Entwickler**: KhassinX
