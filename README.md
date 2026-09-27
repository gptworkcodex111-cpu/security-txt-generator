# Free bilingual `security.txt` generator

A small, standalone browser tool for creating a basic RFC 9116 `security.txt` file in English or Spanish.

**Try it now:** [Open the live generator](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/security-txt-generator.html)

## What it does

- Builds a `security.txt` file from your contact URI, expiry date, preferred languages, and optional policy URLs.
- Validates the basic contact and URL formats before download.
- Keeps all entered values in your browser; it has no backend, analytics, or third-party scripts.
- Downloads a plain-text file you can adapt and publish at `/.well-known/security.txt` over HTTPS.

## Run locally

Open [`index.html`](index.html) in a modern browser. There are no build steps or dependencies.

Review the generated file before publishing. Replace the example contact and confirm the expiry date, domain, and policy links are correct. This basic tool is not legal advice, a security assessment, or authorization to test any system.

## More resources

- [Free disclosure-scope guide](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-disclosure-scope-guide.html)
- [Vulnerability disclosure policy checklist (English)](docs/vulnerability-disclosure-policy-checklist.md)
- [Bilingual security starter kit and response pack](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/)

The full kit and response pack are optional paid resources; the live page lists current contents, prices, and payment details. This project was prepared with AI assistance.

## Español

Generador independiente en el navegador para crear un archivo básico `security.txt` según RFC 9116.

- Crea el archivo con URI de contacto, fecha de vencimiento, idiomas preferidos y URL opcionales de política.
- Valida formatos básicos antes de descargar.
- Mantiene los datos en el navegador; no hay servidor, analítica ni scripts de terceros.
- Descarga un archivo de texto que puedes adaptar y publicar en `/.well-known/security.txt` mediante HTTPS.

### Uso

Abre [`index.html`](index.html) en un navegador moderno. No requiere compilación ni dependencias.

Revisa el archivo antes de publicarlo. Sustituye el contacto de ejemplo y comprueba la fecha de vencimiento, el dominio y los enlaces de política. Esta herramienta básica no es asesoría legal, una evaluación de seguridad ni una autorización para probar sistemas.

Consulta la [guía gratuita de alcance de divulgación](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-disclosure-scope-guide.html) y el [kit bilingüe de seguridad](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/). Los recursos de pago son opcionales; el sitio muestra contenido, precios y detalles de pago actuales.

