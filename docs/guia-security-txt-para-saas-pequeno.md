# Guía práctica para publicar `security.txt` en un SaaS pequeño

Un canal público para reportar vulnerabilidades sirve cuando quienes investigan pueden encontrarlo y el equipo atiende los mensajes. RFC 9116 define `security.txt`, un archivo de texto que publica el canal de contacto y puede enlazar la política de divulgación. Complementa esa política; no la sustituye.

## Publica el archivo en la ubicación indicada

Para un servicio web, usa esta ruta:

```text
https://ejemplo.com/.well-known/security.txt
```

El archivo debe servirse por HTTPS, como texto plano UTF-8. La ruta `/.well-known/` es la ubicación definida por RFC 9116. Puedes conservar `/security.txt` por compatibilidad, pero si lo haces, redirígelo a la ruta `/.well-known/`.

## Incluye los campos obligatorios

Un ejemplo mínimo:

```text
Contact: mailto:seguridad@ejemplo.com
Expires: 2027-01-01T00:00:00Z
```

- **Contact** es obligatorio. Usa un correo, teléfono o página que el equipo revise y que permita recibir reportes.
- **Expires** también es obligatorio. Es una fecha y hora en formato RFC 3339. RFC 9116 recomienda fijarla a menos de un año para evitar que la información quede desactualizada.

Puedes añadir campos opcionales:

```text
Preferred-Languages: es, en
Canonical: https://ejemplo.com/.well-known/security.txt
Policy: https://ejemplo.com/seguridad/divulgacion
```

Indica solo los idiomas que el equipo puede atender. La política debería explicar qué sistemas están dentro del alcance, cómo enviar un reporte y qué condiciones de divulgación o puerto seguro ha adoptado realmente la organización.

## Define el alcance y los permisos en la política

Un archivo recuperado desde un dominio se aplica a ese dominio; no cubre automáticamente sus subdominios ni el dominio principal. Si también cubre productos, servicios u otros hosts, descríbelos expresamente en la política enlazada.

La presencia de `security.txt` no autoriza pruebas de seguridad. La política debe especificar los sistemas permitidos, los límites de las pruebas y cómo reportar los hallazgos.

## Verifica la publicación

Antes de anunciar el archivo:

1. Abre la URL HTTPS exacta desde fuera de la aplicación.
2. Confirma que responde con el contenido esperado como `text/plain; charset=utf-8`.
3. Prueba cada enlace y verifica que lleva al host y página correctos.
4. Confirma que el canal de contacto llega a una persona o equipo que lo monitorea.
5. Programa la renovación antes de la fecha de vencimiento y actualízalo si cambia el proceso.

## Recursos gratuitos y opcionales

El [generador bilingüe gratuito de security.txt](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/security-txt-generator.html) prepara un archivo básico en el navegador; no lo publica por ti. También puedes consultar la [guía gratuita para definir el alcance de divulgación](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-disclosure-scope-guide.html) y la [guía práctica en inglés](security-txt-setup-for-small-saas.md).

Para equipos que prefieren plantillas bilingües listas para adaptar, el [paquete de tres respuestas cuesta 10 USDC](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_u_6MTdr8SsjSLDTbROvpayFq) y el [kit completo de seis plantillas cuesta 25 USDC](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_jMslZWL_-01b4e6Xxv7SpYxr), en Base. Son recursos opcionales; el generador y las guías son gratuitos. El checkout requiere iniciar sesión en FluxA.

*Preparado con ayuda de IA. Esta guía es una lista práctica, no una evaluación de seguridad ni asesoría legal. Consulta RFC 9116 y pide a tu organización revisar su propia política de divulgación.*

## Referencia

- [RFC 9116: formato de archivo para facilitar la divulgación de vulnerabilidades de seguridad](https://www.rfc-editor.org/rfc/rfc9116.html)
