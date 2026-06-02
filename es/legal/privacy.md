---
layout: prose
title: Vellichor — Política de Privacidad
permalink: /es/legal/privacy/
lang: es
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
updated: 2026-05-27
---

# Política de Privacidad

**Fecha de vigencia: 2026-05-27**

Esta es la política de privacidad de **Vellichor**, una app de Q&A sobre PDFs para plataformas Apple desarrollada por **KhassinX**.

La escribimos en lenguaje claro porque queremos que la leas de verdad.

## La versión corta

- **No recolectamos, almacenamos ni transmitimos tus PDFs ni tus consultas sobre ellos.** Vellichor ejecuta Apple Intelligence Foundation Models en tu dispositivo.
- **No tenemos analytics, ni SDKs de tracking, ni servicios de terceros en v1.** Ni Firebase, ni Google Analytics, ni Mixpanel, ni Sentry, ni Crashlytics. Ninguno.
- **No hay sistema de cuentas.** No tienes que registrarte, no nos das un email, no hay contraseña que olvidar.
- **Tu biblioteca y anotaciones se sincronizan entre tus dispositivos vía tu propio iCloud.** Apple lo cifra de extremo a extremo; nosotros nunca lo vemos.
- **Tu compra la verifica Apple, no nosotros.** No guardamos información de pago ni sabemos cuánto pagaste.

## Qué datos maneja Vellichor

### Documentos (tus PDFs)

Vellichor lee los PDFs que importas desde Archivos, Compartir, escaneos con la cámara, drag-and-drop o iCloud Drive. Estos documentos se guardan:

- **En tu dispositivo**, dentro del contenedor de aplicación de Vellichor
- **En tu iCloud Drive personal** bajo la carpeta de Vellichor, si activas sync iCloud (así los mismos documentos aparecen en tus otros dispositivos Apple)

Nosotros — KhassinX — no tenemos acceso a esos documentos en ningún momento. Nunca llegan a un servidor que controlemos. Tampoco llegan a servidores de Apple en forma legible; iCloud Drive usa cifrado de extremo a extremo atado a tu Apple ID.

### Las preguntas que haces y las respuestas que Vellichor genera

Cuando le haces una pregunta a Vellichor sobre un PDF, esa pregunta la procesa Apple Intelligence Foundation Models corriendo localmente en tu iPhone, iPad o Mac. El modelo produce una respuesta usando el contenido del documento como contexto.

- **La pregunta no sale de tu dispositivo.**
- **La respuesta no sale de tu dispositivo.**
- El historial de conversación se guarda en tu dispositivo (y se sincroniza vía tu iCloud personal entre tus dispositivos, si iCloud está activo).

### Anotaciones, highlights y notas

Todo lo que marcas — highlights de texto, notas tipeadas, escritura a mano con Apple Pencil — se guarda en la base privada de CloudKit bajo tu Apple ID. La base privada de CloudKit está cifrada de extremo a extremo; solo tus dispositivos pueden leerla. Nosotros no.

### Estado de suscripción / compra

Vellichor usa **StoreKit 2** (el sistema de compras dentro de la app de Apple) para el desbloqueo Pro de una sola vez. Cuando compras, Apple confirma la transacción directamente con la App Store de tu dispositivo. No corremos un servidor de pagos, no guardamos información de tarjetas y no conocemos tu nombre real, email ni dirección de facturación. Vía la validación anónima de recibo de Apple, solo podemos saber si una instalación dada compró Pro — nada más.

Family Sharing está soportado: si un miembro de tu familia compró Vellichor Pro, tu dispositivo recibe el entitlement automáticamente vía Apple.

### Reportes de crash y diagnósticos

Si Vellichor se cuelga, el sistema estándar de reporte de fallos de Apple puede incluir un reporte anónimo enviado a Apple **si y solo si optaste por compartir vía Ajustes de iOS → Privacidad y Seguridad → Análisis y mejoras → Compartir con desarrolladores de Apps**. Es un mecanismo de Apple, no nuestro. Recibimos logs de crash agregados, totalmente anónimos, a través de App Store Connect; no contienen contenido de documentos, preguntas, respuestas ni información personal identificable.

Si no optaste por compartir analytics con Apple, no recibimos nada.

## Qué datos Vellichor NO maneja

- **Sin SDKs de analytics.** Ni Firebase Analytics, Google Analytics, Mixpanel, Amplitude, Segment, Sentry, Crashlytics, AppsFlyer, Adjust, Branch, Singular, Kochava, Apphud, RevenueCat ni ninguna otra herramienta de telemetría de terceros. Ninguno.
- **Sin publicidad.** Sin redes de anuncios, sin píxeles de tracking, sin recolección de IDFA, sin atribución SKAdNetwork.
- **Sin logins sociales.** Sin "Inicia sesión con Google", sin SDK de Facebook, sin proveedor de identidad de terceros.
- **Sin IA externa.** Vellichor solo usa Apple Intelligence en el dispositivo. En v1 no enviamos tu contenido a OpenAI, Anthropic, Google ni a ningún otro proveedor de IA.

## Niños

Vellichor tiene clasificación 4+ y no contiene contenido objetable. No recolectamos datos de niños a sabiendas porque **no recolectamos datos de nadie**.

## Tus derechos

Como no recolectamos datos, no hay nada que podamos acceder, corregir, eliminar ni exportar a tu pedido. Por supuesto, puedes eliminar la app y (por separado) borrar sus datos de iCloud de tu Apple ID en cualquier momento.

Si vives en una jurisdicción con derechos de privacidad específicos (GDPR en la UE/Reino Unido, CCPA en California, LGPD en Brasil, y otros), esos derechos siguen aplicando, pero su efecto práctico sobre Vellichor es mínimo: no somos el controlador de datos sobre nada tuyo.

## Cambios a esta política

Si alguna vez cambiamos esta política, vamos a actualizar la "Fecha de vigencia" arriba y publicar la nueva versión en esta URL. La versión anterior queda accesible vía el historial de commits de GitHub de este sitio ([KhassinX/vellichor-web](https://github.com/KhassinX/vellichor-web)).

No vamos a expandir retroactivamente lo que recolectamos. Si una feature futura de Vellichor requiere alguna recolección (por ejemplo, un opt-in opcional de bug-reporting), será opt-in y explícito, y esta política se actualizará antes de que esa feature se publique.

## Contacto

- **Consultas de privacidad**: [hello@khassinx.com](mailto:hello@khassinx.com)
- **Reportes de seguridad**: [security@khassinx.com](mailto:security@khassinx.com) ([política](/es/security/))
- **Desarrollador**: KhassinX
