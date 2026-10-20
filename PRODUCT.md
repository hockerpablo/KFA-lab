# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static single file: `index.html` with inline CSS and JS, Google Fonts (Archivo), photos in `fotos/`. No build step.

## Users

Primary: people in Malagueño and nearby Córdoba with a broken iPhone (XR to 16 Pro Max). They usually arrive on a phone and want two things before going to the shop: what the repair will cost, and whether they can trust the lab with the device.

## Product Purpose

KFA Lab is an iPhone repair lab. The site shows prices per model and repair, shows real work from the bench, and turns a visit into a pre-filled inquiry. Success is a local customer who picks their model and repair and sends a message, already knowing the price and what to expect.

## Positioning

- **Board-level work:** microscope diagnosis, microsoldering, reballing, sandwich boards and Face ID. Most local shops only swap parts.
- **Transparent prices:** a published price per model, with labor (USD) separated from the part (ARS, from Mundo Parts) when data exists.
- **Personal attention:** direct contact, and the customer is told what to expect before coming in.

## Operating Context

- Mostly mobile visits. Customers select model → repair → send a pre-filled inquiry.
- Parts come from Córdoba wholesalers: Mundo Parts (main supplier), Fast Cheap, i2C. The owner chose not to name or link them on the public site (2026-10-18), so customers aren't sent to buy parts elsewhere. Public copy says "mayoristas de Córdoba".
- Programming of batteries and screens with JCID V1SE to avoid the "non-genuine part" warning, depending on model and part. This is a capability, not a main selling point.
- Board and Face ID jobs usually take 1 to 2 weeks.
- Address: Peñeñory 598, Malagueño. Monday to Friday, 9 to 20 h.

## Capabilities and Constraints

- Labor in USD is calculated at the day's **average** ("promedio") dollar rate in Córdoba, from https://www.infodolar.com/cotizacion-dolar-localidad-cordoba-provincia-cordoba.aspx (owner, 2026-10-18).
- Screen types, in the owner's words: Incell is the most economical option; OLED has colours and brightness like the original; Autoprogramable is only for cases of a broken IC ID and is higher quality than the others (owner, 2026-10-18).
- The page shows "Precios actualizados el …" from the `PRECIOS_ACTUALIZADOS` constant in `index.html`. Update it whenever prices change.
- A "no prende / no sé qué tiene" diagnosis entry may be offered, but its cost must not be mentioned (owner, 2026-10-18).
- Older models than the price table covers (e.g. iPhone 7 Plus, 8 Plus) are also repaired, by inquiry (owner, 2026-10-18).
- Price table: 26 models × 14 repair variants (`modelos` array in `index.html`). Values are USD, "Consultar", or "No aplica".
- Part prices in ARS for screens, batteries and charging flex (`repuestosPantallas`, `repuestosBaterias`, `repuestosFlexCarga`). `null` means the wholesaler has no data.
- **Prices change often and are edited by hand.** Price and part data must stay in plain, easy-to-edit structures, kept separate from the presentation.
- **WhatsApp is the primary contact:** +54 9 351 572-1212, set as `WHATSAPP = '5493515721212'` in `index.html`. Instagram (@kfa.lab) is the secondary channel.
- Do not promise warranty terms or timeframes beyond those already stated.

## Brand Commitments

- Name: KFA Lab. Instagram: @kfa.lab.
- Voice: Argentine Spanish with voseo ("Elegí tu iPhone", "Escribinos"). Direct, factual and technical without jargon. Short sentences.

## Evidence on Hand

- Real lab photos in `fotos/`: repaired devices (7 Plus to 12), boards, reballing, sandwich board, microscope, bench, screens and batteries in stock, the JCID programmer.
- Real price data in `index.html`.
- None yet: testimonials, review counts, warranty policy, number of repairs. Never fabricate these.

## Product Principles

1. Price before persuasion: the customer should find their exact price in seconds.
2. Show the bench: real photos of real work are the proof. No stock imagery.
3. Honest about uncertainty: "Consultar" and "No aplica" are stated plainly, and board work is diagnosed before it is quoted.
4. Every path ends in a direct, pre-filled conversation with the lab.
5. Data stays editable: price updates must never require touching the layout.

## Accessibility & Inclusion

No product-specific requirement established. Follow the general web baseline, with a mobile-first reading context.
