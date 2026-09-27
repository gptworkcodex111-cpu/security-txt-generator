# A practical `security.txt` setup for a small SaaS

A public vulnerability-reporting address is useful only if researchers can find it and someone reads it. RFC 9116 defines `security.txt`, a small plain-text file that points researchers toward an organization's reporting channel and disclosure policy. It complements a policy; it does not replace one.

## Put the file in the well-known location

For a web service, publish it at:

```text
https://example.com/.well-known/security.txt
```

Serve it over HTTPS as UTF-8 plain text. RFC 9116 requires the `/.well-known/` path; a root-level `/security.txt` may be kept as a compatibility redirect, but it is not the preferred location.

## Start with the required fields

A minimal example is:

```text
Contact: mailto:security@example.com
Expires: 2027-01-01T00:00:00Z
```

- **Contact** is required. Use an inbox or web form that someone actually monitors. A contact method is only useful if reports are received and routed.
- **Expires** is required and must be a date-time. RFC 9116 recommends keeping it less than a year in the future. Set a calendar reminder to renew it before it becomes stale.

Optional fields can make the file more useful:

```text
Preferred-Languages: en, es
Canonical: https://example.com/.well-known/security.txt
Policy: https://example.com/security/disclosure
```

List only languages your team can support. The policy link should explain the scope, how to report, what information to include, and any safe-harbor or coordinated-disclosure terms that the organization has actually adopted.

## Be precise about scope and permission

A `security.txt` file applies to the domain where it is retrieved; it does not automatically cover every subdomain or parent domain. Name in-scope systems in the linked policy.

The file itself does **not** grant permission to test. RFC 9116 explicitly warns researchers not to infer authorization from the presence or absence of the file. Keep testing instructions and boundaries in a policy that the organization has reviewed.

## Check the deployment

Before announcing the file:

1. Fetch the exact HTTPS URL from outside the application.
2. Confirm it returns the intended text with `Content-Type: text/plain; charset=utf-8`.
3. Check that every listed link points to the intended host and page.
4. Confirm the contact route reaches a monitored team.
5. Record the expiry date and renew the file when the process or contact changes.

## Try the free generator

The [bilingual security.txt generator](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/security-txt-generator.html) builds a basic file locally in your browser. Your entries stay on the page; the tool does not publish the file for you. Review the contact, scope and expiry before deploying it.

There is also a [free disclosure-scope guide](https://indie-saas-security-kit.edisoncristoferlopez.chatgpt.site/vulnerability-disclosure-scope-guide.html). For teams that want ready-to-adapt bilingual intake and response templates, the [three-message pack is $10 USDC](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_u_6MTdr8SsjSLDTbROvpayFq) and the [six-template kit is $25 USDC](https://agentwallet.fluxapay.xyz/pay/paymentlink/pl_jMslZWL_-01b4e6Xxv7SpYxr), paid on Base. These are optional downloads; the generator and guide are free. The checkout requires a FluxA sign-in.

*Prepared with AI assistance. This is a practical checklist, not a security assessment or legal advice. Check RFC 9116 and have your organization review its own disclosure policy.*

## Reference

- [RFC 9116: A File Format to Aid in Security Vulnerability Disclosure](https://www.rfc-editor.org/rfc/rfc9116.html)
