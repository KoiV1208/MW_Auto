# MW Automobile — Website

Moderne, responsive Website für **MW Automobile** (Michael Wirtz), Fahrzeugvermittlung
für Cabrios & Sportwagen in Rösrath bei Köln. Inspiriert von der bestehenden Seite
[mwauto.de](https://mwauto.de), neu konzipiert im Premium-Dark-Design mit
Orange-Gold-Akzent.

## Tech-Stack

Rein statisches HTML/CSS/JS — kein Build-Prozess, kein Framework. Läuft direkt im
Browser oder auf jedem statischen Hosting (GitHub Pages, Netlify, Vercel, klassisches
Webhosting).

```
/
├── index.html          Startseite
├── ueber-uns.html       Über Michael Wirtz
├── fahrzeuge.html        Fahrzeugbestand (mit Filter)
├── ablauf.html            Ablauf Kauf & Verkauf
├── referenzen.html        Kundenstimmen
├── faq.html                Häufige Fragen (Accordion)
├── kontakt.html            Kontaktformular & Infos
├── impressum.html          Impressum (Platzhalter, rechtlich prüfen)
├── datenschutz.html        Datenschutzerklärung (Platzhalter, rechtlich prüfen)
└── assets/
    ├── css/style.css       Design-System (Farben, Layout, Komponenten, Responsive)
    ├── js/main.js           Mobile-Menü, FAQ-Accordion, Filter, Scroll-Reveal
    └── img/favicon.svg      Favicon (MW-Monogramm)
```

## Lokal ansehen

Kein Build nötig — einfach `index.html` im Browser öffnen, oder für sauberere
relative Pfade einen einfachen lokalen Server starten:

```bash
python3 -m http.server 8080
# dann im Browser: http://localhost:8080
```

## Design

- **Farben:** Dunkles Anthrazit/Schwarz (`--bg`) mit Orange-Gold-Akzent (`--accent`).
  Alle Tokens zentral in `assets/css/style.css` (`:root`) definierbar.
- **Typografie:** „Playfair Display“ (Überschriften) + „Inter“ (Fließtext), via Google Fonts.
- **Responsive:** Mobile-first mit Breakpoints bei 1024px / 860px / 640px, inkl.
  Hamburger-Menü für kleine Bildschirme.
- **Platzhalter:** Fahrzeug- und Portraitbilder sind bewusst als edle SVG-Line-Art-
  Grafiken umgesetzt (kein Hotlinking auf externe Stockfotos, dadurch keine toten
  Bilder). Vor dem Live-Gang durch echte Fotos (Fahrzeuge, Michael Wirtz) ersetzen.

## Offene Punkte vor dem Live-Gang

1. **Kontaktformular:** aktuell nur optisch funktionsfähig (kein Backend). Für den
   Live-Betrieb z. B. an [Formspree](https://formspree.io) oder [Web3Forms](https://web3forms.com)
   anbinden (Formular-`action`/`fetch` in `kontakt.html` / `main.js` ergänzen).
2. **Impressum & Datenschutz:** enthalten Platzhalter (z. B. USt-ID) — vor
   Veröffentlichung rechtlich prüfen lassen.
3. **Bilder:** SVG-Platzhalter durch echte Fotos (Fahrzeuge, Portrait) ersetzen.
4. **Fahrzeugbestand:** Beispiel-Fahrzeuge in `fahrzeuge.html` / `index.html` durch
   echten, aktuellen Bestand ersetzen oder dynamisch aus mobile.de einbinden.
