# PatentScreen

Screening af patentansøgningers bilag for formelle krav jf. PA Guidelines – Formalitetsbehandling og intern procedure FSP 3.2.2 (v40).

Statisk webapp — ingen build, ingen backend. Deploy direkte:

- **Vercel**: Importér repo'et, Framework preset: *Other*. Publiceringsmappe er roden.
- **GitHub Pages**: Aktivér Pages på branchen (index.html ligger i roden).
- **Lokalt**: Åbn `index.html` i en browser, eller `npx serve .`

## Funktionalitet

- Upload af ansøgningens bilag som PDF'er.
- Tekst udtrækkes i browseren med pdf.js — filindholdet tjekkes reelt, ikke blot tilstedeværelse.
- Regelsæt: PA Guidelines (PL § 8 / BEK § 3) + interne tjekpunkter fra FSP 3.2.2 med punkt henvisninger.
- Henlæggelsesflag pr. mangel (pkt. 9.1) og anbefalet FM-brev (1–4) jf. brevgenerator-udelukkelsesmetoden.
- Gebyropgørelse: 3.000 kr. + 300 kr. pr. krav over 10 (kun opgørelse — betalingsverifikation foretages i Easyflow).
- Score 1–10 og rapport med handlingsliste, henvisninger og opgørelser.

## Struktur

```
index.html   – hele appen (React, Tailwind og pdf.js via CDN)
README.md
```

## Bemærkninger

- Ved tvivl gælder guidelines altid.
- Tjeks der kræver sagssystemdata fra Easyflow (fasefrister, stikord, betaling, årsgebyrer) er bevidst udeladt fra den automatiske screening.
- Regelsættet vedligeholdes i `RULES`-objektet i index.html.
