---
title: "Custom Domains"
canonical: "https://dokki.one/pub/docs/custom-domains"
source_url: "https://dokki.one/pub/docs/custom-domains"
updated_at: "2026-07-20T11:10:55.018+00:00"
generated_by: Dokki
---

# Custom Domains

A custom domain lets a Dokki public site use an address you own, such as docs.example.com . Before you begin Create and activate the public site first. Choose a domain or subdomain you are allowed to

Canonical source: [https://dokki.one/pub/docs/custom-domains](https://dokki.one/pub/docs/custom-domains)

A custom domain lets a Dokki public site use an address you own, such as `docs.example.com`.

## Before you begin

- Create and activate the public site first.
- Choose a domain or subdomain you are allowed to manage.
- Make sure you can edit its DNS records.

## Connect the domain

- Open **Publish → Site settings**.
- Add the custom domain.
- Copy the DNS record shown by Dokki into your DNS provider.
- Return to Dokki and choose **Verify DNS**.
- Wait for both the domain and its security certificate to become active, then open the domain in a browser.

## DNS changes can take time

DNS updates are not always immediate. If verification is still pending, confirm that the record name and value exactly match the values shown in Dokki, remove conflicting records, and try again later.

## Use the custom domain

After activation, public links and page metadata use the custom domain. Listing, languages, publishing updates, and site navigation continue to work as they do on the default Dokki address.

## Remove or replace a domain

Remove the domain from Site settings before pointing it elsewhere. The Dokki site remains available at its default public address while the site itself is active.

## Troubleshooting

- **Pending** — wait for DNS to update, then verify again.
- **Record not found** — compare the DNS name and value with the values shown in Dokki.
- **Domain already used** — remove it from the other Dokki site before adding it here.
- **Site opens at the default address only** — confirm the custom domain is active, not merely added.

---

Published from Dokki.
