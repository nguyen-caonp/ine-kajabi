# Ine Røyert – business profile (foundation document)

Client of AweSM. This repo holds work for Ine's business: email templates, automations notes, and this profile.
Last updated: 2026-11-23. The fuller voice, audience and strategy reference is AweSM's «Ine Røyert – Copy & Strategy Guide» (15 Oct 2026) in [docs/copy-strategy-guide.md](docs/copy-strategy-guide.md) – read it before writing any copy; this file adds what changed since.

## Who
- **Ine Røyert** – mentaltrener (mental trainer), lederutvikler (leadership developer), author of the book *Du er rå!*
- Company: **Pure Performance** (copyright line in her books). Website: www.ineroyert.no. Contact: team@ineroyert.no.
- Method: mental training + NLP coaching tools + "best practice" from her own life and hundreds of clients.
- Background: almost two decades in business (sales records, project management, TV production) before starting her own company.
- Her own story (adversity, 2024 when «alt raknet») is part of her content; use only what she has published herself.
- Mission line: make psychology and mental strength training simple and accessible for everyone; "spille andre gode".
- Instagram: @ineroyert.mentaltrener · LinkedIn: ine-røyert-6a154280 · Facebook: inecoaching

## Audience
- Mainly Norwegian women, roughly 30–50, who run their own business or carry heavy leadership responsibility and have become their own bottleneck: racing thoughts, a head that never switches off, never quite "land".
- Core pains she speaks to: capacity, energy, overload, self-leadership, not being able to switch off, self-confidence.
- Language: **Norwegian (bokmål)** for all customer-facing copy. Internal/team communication with AweSM is in English.

## Voice
- Warm, personal, direct, encouraging, a bit playful (emoji, "Du er rå!", "Jeg heier på deg"). First person, speaks to "du".
- Recurring phrases: "Litt blir mye over tid", "Mentaltrening er ferskvare", "Du er rå – om du velger det", "Play is the way".
- Signs off "Varm hilsen, Ine" / "Klem, Ine". Signature: *Ine Røyert – Mentaltrener · Lederutvikler · Forfatter av «Du er rå»*.
- Positions mental training as training, not therapy; refers to professionals for trauma.

## Products and offers
| Product | Format | Price | Sold via |
|---|---|---|---|
| **Du er rå!** (book) – Norli bestseller list at launch | Physical book, can be signed | 349 kr incl. shipping | **edpay** checkout embedded on /bok/mentaltrening (Vipps) |
| **Du er rå! Treningsboka** (workbook, launching Nov 2026) | 59-page fillable PDF: 3 parts, 23 core exercises, 4-week programme, toolbox | 199 kr regular · 99 kr EdPay upsell with the book · 99 kr Black Week (23–30 Nov) | Kajabi offer "Arbeidsbok: DU ER RÅ!" (draft) + EdPay upsell |
| **KAPASITETSKODEN™** (flagship) | 12-week group training programme: 6 steps, live coaching every other week, bonus masterclasses, 12 months access | 14.900 kr webinar / 17.900 kr ordinary / 12 × 1.490 kr | Kajabi, sold through webinar funnel |
| Meant 4 More | Older name for the same programme; to be retired (community may stay as alumni space) | 11.900 kr offer still published | Kajabi |
| 1:1 mentaltrening og coaching | Premium | Application only, fully booked 2026 | — |
| Smakebit Hypnobreathwork | Digital download | 149 kr | Kajabi |

Free lead magnets: mindset quiz (/mindsetquiz), book excerpt (/bok/mentaltrening/free), livshjulet, huskeliste, yoga nidra, 5-dagers mental reset, newsletter, free webinars.
Book resources page for buyers: www.ineroyert.no/ressurser/bok.

## Funnel
1. Content (Instagram/LinkedIn), talks (e.g. Kamille-weekend "strategisamling") and lead magnets → email list (1.715 contacts Oct 2026; about 1 300 reachable by broadcast).
2. Free live webinar «Koster suksessen deg for mye?» (Zoom, ~90 min, /gratis-webinar-1) → email sequence (repo `webinar-emails/`) → KAPASITETSKODEN™.
3. Downsell for non-buyers: the book (`se9-downsell-bok.html`). Book buyers → workbook upsell → later programmes.

## Tech stack
- **Kajabi** (site 97489, "Ine Royert"): website, landing pages, offers, courses, community, email broadcasts, automations.
- **edpay** (app.edpay.no): book checkout (embed `edpayBookCheckout(418, 10131, …)`). After an order, edpay grants the Kajabi offer "DU ER RÅ!" via webhook.
- **n8n** (AweSM account): workflow "INE – edpay bokkjøp → Kajabi (Form.bokkjøp)" – built, **inactive**, pending test.
- Zoom for live webinars.

## Key Kajabi IDs
- Offer "DU ER RÅ!" 2150697252 · Automation "When offer is granted…" 442007 (tag `8. TAG.bokkjøp` + "Gratulerer!🎉" email)
- Form "Form.bokkjøp (edpay – ikke på side)" 2149769236
- Workbook: offer 2151503279 (draft, 199 kr), product 2149627752
- Tags: `8. TAG.bokkjøp` (book buyers), `01. Main Main List – Leads`

## Open issues / decisions
- **Book buyers get a Kajabi login email** because edpay *grants* an offer. The planned fix is edpay → n8n → Form.bokkjøp, then switching automation 442007's trigger to the form. Needs a test address and someone with edpay admin access.
- Workbook: waiting for the final PDF (new cover + proofread), Ine's approval of the prices, a Black Week coupon, and the EdPay upsell webhook. Naming: PDF says "Treningsboka", Kajabi says "Arbeidsbok" – align.
- Don't send customer-facing changes (emails, broadcasts, publishing) without approval from the AweSM team or Ine.
