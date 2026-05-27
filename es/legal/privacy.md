---
layout: prose
lang: es
title: Política de privacidad
description: Política de privacidad para vellichor.khassinx.com y la próxima app Vellichor. Recolección de datos cero por diseño.
permalink: /es/legal/privacy/
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
canonical_pt: /pt-BR/legal/privacy/
canonical_de: /de/legal/privacy/
updated: 2026-05-27
---

## Resumen

No recolectamos datos personales a través de este sitio ni de la app Vellichor. No hay analytics, ni cookies, ni rastreadores de terceros, ni sistema de cuentas. Los PDFs que procesás con Vellichor se leen localmente con los Apple Intelligence Foundation Models on-device — nunca salen de tu dispositivo.

## Sobre este sitio (`vellichor.khassinx.com`)

El sitio es HTML estático servido desde GitHub Pages con Cloudflare como proxy de red para performance y headers de seguridad.

- **Sin analytics.** Sin Google Analytics, sin Plausible, sin Fathom, sin analytics propios.
- **Sin cookies.** El sitio no setea cookies. Cloudflare puede setear una cookie corta para protección anti-bot; no podemos desactivarla y no te identifica.
- **Sin scripts de terceros.** Sin embeds sociales, sin chat widgets, sin píxeles publicitarios.
- **Sin sistema de cuentas.** No hay nada para registrarse en este sitio.

**Qué loguean nuestros hosts.** GitHub Pages (el servidor estático) y Cloudflare (el proxy de red) registran metadata HTTP estándar como IP, user-agent, timestamp y URL pedida. No tenemos acceso a analytics a nivel usuario en ninguno. Esos logs se rigen por las políticas de [GitHub](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement) y [Cloudflare](https://www.cloudflare.com/privacypolicy/).

## Sobre la app Vellichor (postura pre-lanzamiento)

La app Vellichor para iOS/iPadOS/macOS/watchOS, cuando se lance, va a seguir estos principios:

- **Los PDFs se procesan en tu dispositivo.** Toda inferencia de modelos de lenguaje usa los Apple Intelligence Foundation Models corriendo localmente. Los PDFs nunca se suben a servidores nuestros; no operamos servidores que reciban tus documentos.
- **La sincronización usa tu iCloud.** El sync entre dispositivos usa CloudKit Private Database e iCloud Drive bajo tu Apple ID. Los datos viven en tu iCloud — nosotros no accedemos.
- **Sin telemetría.** Sin frameworks de crash reporting que envíen datos personales, sin event analytics, sin instrumentación de uso. Los reportes de crash estándar de Apple (si optás por enviarlos en Ajustes del sistema) se rigen por la política de Apple.
- **Privacy Manifest.** El `PrivacyInfo.xcprivacy` de la app va a declarar cero recolección de datos. La nutrition label de App Store va a decir "Data Not Collected" en todas las categorías.

La Política de Privacidad definitiva integrada en la app va a reflejar el comportamiento final al momento de lanzar y se publicará acá.

## Contacto por email

Si nos escribís a cualquier dirección `@khassinx.com`, recibimos tu mensaje y tu dirección de respuesta a través de nuestro proveedor de email (Proton Mail). Retenemos esa correspondencia para manejar la conversación y eventual follow-up. No te agregamos a ninguna lista de mailing.

## Tus derechos

No nos diste datos personales a través de este sitio, así que no hay nada tuyo que borrar o exportar acá. Si nos escribiste por email, podés pedir que borremos esa correspondencia en cualquier momento.

## Cambios

Podemos actualizar esta política a medida que el sitio o la app evolucionen. Los cambios materiales se reflejan en la fecha "Last updated" arriba.

## Contacto

Preguntas sobre esta política: [`legal@khassinx.com`](mailto:legal@khassinx.com).
