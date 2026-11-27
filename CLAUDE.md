# Ine Røyert – business profile (foundation document)

Client of AweSM. This repo holds work for Ine's business: email templates, automations notes, and this profile.
Last updated: 2026-11-27. The fuller voice, audience and strategy reference is AweSM's «Ine Røyert – Copy & Strategy Guide» (15 Oct 2026) in [docs/copy-strategy-guide.md](docs/copy-strategy-guide.md) – read it before writing any copy; this file adds what changed since.

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
| **Du er rå!** (book) – Norli bestseller list at launch | Physical hardcover, signed with a personal greeting. About 88 left on 27 Nov 2026; next print run will be softcover | 349 kr incl. shipping | **edpay** checkout embedded on /bok/mentaltrening (Vipps). Sold direct since May 2026 (before that only in bookstores) |
| **Du er rå! Treningsboka** (digital workbook, launched 27 Nov 2026) | PDF, about 45 pages, delivered as a Kajabi digital download | 199 kr regular · 99 kr closed offer for book owners (Black Week only) · planned 99 kr EdPay upsell with the book (not set up yet) | Kajabi offers «Treningsboka: DU ER RÅ!» and «Treningsboka – for deg som har DU ER RÅ!» (both published) |
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
- Treningsboka: offer 2151503279 (199 kr), closed offer 2151543359 (99 kr), product 2149627752 (still titled «Arbeidsbok: DU ER RÅ!» – rename in admin), cover image = media 5841795
- Tags: `8. TAG.bokkjøp` 2149841173 (book buyers), `BW26 – Treningsboka gratis` 2150480262, `01. Main Main List – Leads`
- Book sales page theme 2157842897 (one custom-code section 1792100000001 + BW26 banner section `bw26_banner`)

## Black Week 2026 campaign (27–30 Nov)
**Decision:** no discount on the book. The book was already selling about two a day at full price, stock is low, and a bonus makes no price claim (no Norwegian previous-price rules). Black Week value = Treningsboka + a live session.

**Offer**
| Who | Gets | Price |
|---|---|---|
| Anyone buying the book 27–30 Nov | Book (signed) + Treningsboka free + live «Kom i gang» session | 349 kr |
| Book bought 1–26 Nov (49 people) | Treningsboka free – granted 27 Nov via tag `BW26 – Treningsboka gratis` | 0 kr |
| Book bought May–Oct (~142 subscribed) | Closed offer: Treningsboka + live session (not linked on site) | 99 kr |

- Live «Kom i gang» session: **Thursday 14 January 2027 at 19:00**. Meant to introduce the Mental Fitness Challenge / KAPASITETSKODEN™.
- Christmas delivery: last order date **15 December**.
- Gifts: buyer replies to the order confirmation with the recipient's email → team grants the Treningsboka offer to the recipient manually in Kajabi.
- Message: «Boka ga deg kunnskapen. Nå får du treningsprogrammet.» Christmas gift angle in every email, own email on Sunday.

**Kajabi setup**
- Automation 1764796 «BW26 – Treningsboka gratis til bokkjøpere» (published): triggers = offer DU ER RÅ! granted OR tag `BW26 – Treningsboka gratis` added → grants offer 2151503279 with Kajabi's access email.
- Banner section `bw26_banner` at the top of /bok/mentaltrening (+ matching CSS in the theme's global css).
- Checkout pages for both Treningsboka offers have Norwegian copy and the cover image.
- Segments: `BW26 – har ikke boka` 2148757311 · `BW26 – har boka, uten Treningsboka` 2148757423 · `BW26 – kjøpere av Treningsboka` 2148757312 · last-call segments 2148757324 (clicked 4a) and 2148757426 (clicked new 4b). Old segments `BW26 – har boka` 2148757310 and 2148757326 are superseded.

**Emails (Kajabi broadcasts, sent manually by the AweSM team; the time is in each name)**
| Broadcast | When | To |
|---|---|---|
| 1 Opening 2159013824 | Fri 27.11 11:00 | No book (≈1 169) |
| 2 Closed offer 2159014783 | Fri 27.11 11:30 | Book owners without Treningsboka (≈142) |
| 3 Christmas 2159013830 | Sun 29.11 09:00 | No book |
| 4a Last day 2159013832 | Mon 30.11 07:30 | No book |
| 4b Last day 2159014784 | Mon 30.11 07:45 | Book owners without Treningsboka |
| 5a / 5b Last call 2159013843 / 2159014790 | Mon 30.11 22:30 | Clicked 4a / 4b and haven't bought |
| 6 Welcome 2159013834 | Tue 1.12 09:00 | Everyone with Treningsboka |

Drafts titled «SLETT – gammel …» (2159013829, 2159013833, 2159013855) had the wrong segment – delete, never send.

**On 1 December**
- Unpublish automation 1764796 (otherwise every future book buyer gets Treningsboka free).
- Unpublish the 99 kr offer 2151543359.
- Remove `bw26_banner` from the book page's `content_for_index` (and its CSS).
- Send email 6; afterwards plan the Zoom link email for 14 January.
- Record results (books sold, Treningsboka sales, live-session sign-ups) for next November.

## Open issues / decisions
- **Book buyers get a Kajabi login email** because edpay *grants* an offer. Since Black Week this email now leads to Treningsboka, so it makes sense for campaign buyers. The original fix (edpay → n8n → Form.bokkjøp, then switching automation 442007's trigger to the form) is on hold until after Black Week; revisit whether it's still wanted. Don't change the edpay webhook during a campaign.
- Ine to decide: earlier book buyers (May–Oct) – keep the 99 kr closed offer (recommended) or give Treningsboka free as a thank-you.
- Kajabi's standard offer-grant (access) email: check its wording/language in Settings → Emails – every book buyer now receives it.
- About 1 000+ readers bought the book in bookstores and aren't tagged in Kajabi; they are in the «har ikke boka» group.
- EdPay upsell for Treningsboka (99 kr with the book) is not set up yet.
- Workbook vs. strategy: the guide says to avoid new one-off products until the flagship sells predictably. Make Treningsboka feed the flagship instead – add a KAPASITETSKODEN™/webinar invite to its last page (currently only «Les mer: www.ineroyert.no»), in line with the guide's priority 8.
- Don't send customer-facing changes (emails, broadcasts, publishing) without approval from the AweSM team or Ine.
