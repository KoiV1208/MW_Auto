# MW Automobile — Website

Moderne, responsive Website für **MW Automobile** (Michael Wirtz), Fahrzeugvermittlung
für Cabrios & Sportwagen in Rösrath bei Köln. Inspiriert von der bestehenden Seite
[mwauto.de](https://mwauto.de) sowie einem eigenen Design-Entwurf des Kunden;
umgesetzt in einem hellen, fotografiegetriebenen Design mit kräftiger, großgeschriebener
Typografie und Orange als Markenfarbe.

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

- **Farben:** Weiß/helles Warmgrau (`--bg`, `--bg-alt`) im Wechsel mit dunklen Bändern
  (`--bg-dark`, z. B. USP-, Testimonial- und Footer-Bereich) und Orange als Akzent
  (`--accent`). Alle Tokens zentral in `assets/css/style.css` (`:root`) definierbar.
- **Typografie:** „Poppins“ (fett, großgeschrieben, für Überschriften/Buttons/Labels) +
  „Inter“ (Fließtext), via Google Fonts.
- **Responsive:** Mobile-first mit Breakpoints bei 1024px / 860px / 640px, inkl.
  Hamburger-Menü für kleine Bildschirme.
- **Bilder:** Hero, Fahrzeugkarten, CTA-Banner und die Porträt-/„Über mich“-Fläche
  nutzen lizenzfreie Platzhalter-Fotos von [Unsplash](https://unsplash.com) (direkt
  verlinkt über `images.unsplash.com`). Für die Porträt-Fläche wurde bewusst ein
  gesichtsloses Motiv (Hände am Lenkrad) gewählt statt eines Fremdfotos, das
  fälschlich als Michael Wirtz durchgehen könnte. Vor dem Live-Gang durch echte
  Fotos (Fahrzeugbestand, Porträt von Michael Wirtz) ersetzen.

## Offene Punkte vor dem Live-Gang

1. **Kontaktformular:** aktuell nur optisch funktionsfähig (kein Backend). Für den
   Live-Betrieb z. B. an [Formspree](https://formspree.io) oder [Web3Forms](https://web3forms.com)
   anbinden (Formular-`action`/`fetch` in `kontakt.html` / `main.js` ergänzen).
2. **Impressum & Datenschutz:** enthalten Platzhalter (z. B. USt-ID) — vor
   Veröffentlichung rechtlich prüfen lassen.
3. **Bilder:** Unsplash-Platzhalterfotos durch echte Fotos (Fahrzeugbestand, Porträt
   von Michael Wirtz) ersetzen — Pfade liegen in `index.html`, `fahrzeuge.html`,
   `ueber-uns.html` und `assets/css/style.css` (Hero- & CTA-Hintergrund).
4. **Fahrzeugbestand:** Beispiel-Fahrzeuge in `fahrzeuge.html` / `index.html` durch
   echten, aktuellen Bestand ersetzen oder dynamisch aus mobile.de einbinden.
5. **Bewertungen:** „4,8 von 84 Bewertungen“ ist ein Platzhalterwert — durch die
   echte mobile.de-Bewertung ersetzen.
