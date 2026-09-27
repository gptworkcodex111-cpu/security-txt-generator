# Free bilingual `security.txt` generator

A small, standalone browser tool for creating a basic RFC 9116 `security.txt` file in English or Spanish.

**Try it now:** [Open the live generator](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/security-txt-generator.html)

## Optional ready-to-use templates

For teams that want prepared disclosure replies and an operating workflow:

- [Three-message English/Spanish response pack — 10 USDC on Base](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_u_6MTdr8SsjSLDTbROvpayFq): report received, safe clarification, and status or closure.
- [Complete six-template English/Spanish kit — 25 USDC on Base](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_jMslZWL_-01b4e6Xxv7SpYxr): scope, safe test plan, report, triage, remediation, and security contact page.

FluxA delivers the text resource after confirmed payment. Checkout requires sign-in. The generator and guides below remain free.

## What it does

- Builds a `security.txt` file from your contact URI, expiry date, preferred languages, and optional policy URLs.
- Validates the basic contact and URL formats before download.
- Keeps all entered values in your browser; it has no backend, analytics, or third-party scripts.
- Downloads a plain-text file you can adapt and publish at `/.well-known/security.txt` over HTTPS.

## Run locally

Open [`index.html`](index.html) in a modern browser. There are no build steps or dependencies.

Review the generated file before publishing. Replace the example contact and confirm the expiry date, domain, and policy links are correct. This basic tool is not legal advice, a security assessment, or authorization to test any system.

## Free resources

- [Free disclosure-scope guide](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-disclosure-scope-guide.html)
- [Practical vulnerability disclosure policy writing guide](docs/vulnerability-disclosure-policy-writing-guide.md)
- [How to respond to a vulnerability report (English/Spanish)](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-report-response-templates.html)
- [Practical security.txt setup for a small SaaS](docs/security-txt-setup-for-small-saas.md)
- [Ignlab Launch listing](https://launch.ignlab.net/t/indie-saas-security-starter-kit)
- [Vulnerability disclosure policy checklist (English)](docs/vulnerability-disclosure-policy-checklist.md)
- [Bilingual security starter kit and response pack](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/)

This project was prepared with AI assistance.

## Español

Generador independiente en el navegador para crear un archivo básico `security.txt` según RFC 9116.

- Crea el archivo con URI de contacto, fecha de vencimiento, idiomas preferidos y URL opcionales de política.
- Valida formatos básicos antes de descargar.
- Mantiene los datos en el navegador; no hay servidor, analítica ni scripts de terceros.
- Descarga un archivo de texto que puedes adaptar y publicar en `/.well-known/security.txt` mediante HTTPS.

### Uso

Abre [`index.html`](index.html) en un navegador moderno. No requiere compilación ni dependencias.

Revisa el archivo antes de publicarlo. Sustituye el contacto de ejemplo y comprueba la fecha de vencimiento, el dominio y los enlaces de política. Esta herramienta básica no es asesoría legal, una evaluación de seguridad ni una autorización para probar sistemas.

### Guía gratuita

Consulta la [guía práctica en español para publicar security.txt](docs/guia-security-txt-para-saas-pequeno.md), que explica la ruta, los campos obligatorios, el alcance y las comprobaciones de publicación.

- [Guía práctica para redactar una política de divulgación de vulnerabilidades](docs/guia-politica-divulgacion-vulnerabilidades.md)

También puedes consultar la [guía bilingüe para responder reportes de vulnerabilidad](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-report-response-templates.html#espanol).

### Plantillas opcionales de pago

- [Paquete de tres respuestas bilingües — 10 USDC en Base](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_u_6MTdr8SsjSLDTbROvpayFq): recepción del reporte, aclaración segura y actualización o cierre.
- [Kit completo de seis plantillas bilingües — 25 USDC en Base](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_jMslZWL_-01b4e6Xxv7SpYxr): alcance, plan de prueba seguro, reporte, triaje, corrección y página de contacto.

FluxA entrega el recurso de texto después de confirmar el pago. El checkout requiere iniciar sesión. El generador y las guías mencionadas arriba son gratis.

Consulta la [guía gratuita de alcance de divulgación](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-disclosure-scope-guide.html) y el [kit bilingüe de seguridad](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/).
