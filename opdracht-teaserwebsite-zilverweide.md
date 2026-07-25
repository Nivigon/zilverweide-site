# Opdracht: teaserwebsite De Rozen van Zilverweide

## Doel

E�n eenvoudige pagina waar ik mensen naartoe kan sturen ("kijk maar even op zilverweide.nl"). De bezoeker kijkt vooral op een telefoon, en de link wordt vaak via WhatsApp gedeeld. De pagina moet in ongeveer dertig seconden sfeer en nieuwsgierigheid opwekken. Hoofdactie: volgen op Instagram. Tweede, kleinere actie: aanmelden als playtester via een mailtje.

Geen verkoop. Geen prijzen, geen data, geen boekingssysteem.

## Techniek

- Eén zelfstandig `index.html` bestand. Vanilla HTML/CSS/JS, geen frameworks, geen build-stap.
- Mobile-first: ontworpen voor een telefoon in staand formaat, schaalt netjes mee naar desktop en liggende schermen.
- Verticaal scrollen is hier toegestaan en gewenst (dit is een website, niet het spel).
- Snel ladend en licht. Enige externe afhankelijkheid: Google Fonts (Cinzel en Crimson Text).
- Respecteer `prefers-reduced-motion`. Zichtbare focus-stijlen voor toetsenbord.
- Als je een frontend-design skill beschikbaar hebt, gebruik die, maar de huisstijl hieronder is leidend en staat vast.

## Huisstijl (staat vast, exact overnemen)

- Achtergrond: `#0d0a06`
- Goud: `--gold: #c9a84c`
- Gedimd goud: `--gold-dim: #8a6f32`
- Perkament: `--parchment: #f5ead6`
- Koppen: Cinzel. Lopende tekst: Crimson Text.
- Sfeer: donker, filmisch, veel zwart, spaarzaam en gericht goud. Denk aan een oud sprookjesboek bij lantaarnlicht, niet aan een moderne startup-site.
- Tweede accent: het aangeleverde beeldmateriaal gloeit koud zilverblauw. Dat blauw mag als tweede accentkleur terugkomen (definieer een `--zilverblauw`, afgeleid van de gloed in de beelden), bijvoorbeeld in subtiele gloed-effecten of scheidingslijnen. Goud blijft leidend in typografie en knoppen. Probeer het beeldmateriaal niet goud in te kleuren, het contrast tussen koud blauw (de magie) en warm goud (de mensenwereld) is de bedoeling.

## Beschikbaar beeldmateriaal

In de map `beelden/` staan twee definitieve afbeeldingen. Gebruik ze direct, dit zijn geen plekhouders:

- `splash.jpg` (staand): een veld vol gloeiende blauwe rozen met twee figuren in mantels. Dit is het herobeeld. Zorg dat beide figuren en een deel van het rozenveld zichtbaar blijven op zowel telefoon als desktop, en dat de titel leesbaar blijft (bijvoorbeeld met een donkere verloop-overlay onderaan of bovenaan het beeld).
- `heks.jpg` (liggend): een gehoornde gedaante met gloeiende blauwe ogen. Gebruik dit als eerste sfeerbeeld in de beeldenreeks, en maak er ook de uitsnede van voor het Open Graph-voorbeeldbeeld (1200x630). Houd bij die uitsnede het gezicht gecentreerd.

De overige sfeerbeelden blijven plekhouders zoals hieronder beschreven.

## Metadata en linkvoorbeeld (verplicht onderdeel)

De eerste indruk is vaak het linkvoorbeeld in WhatsApp, niet de site zelf. Daarom verplicht:

- Open Graph en Twitter Card meta-tags: titel "De Rozen van Zilverweide", een korte omschrijving in dezelfde toon als de heldenzin, en een voorbeeldbeeld. Plekhouder voor het beeld: `[Placeholder: og-voorbeeldbeeld]` (aanbevolen formaat 1200x630).
- Een nette paginatitel in het browsertabblad: "De Rozen van Zilverweide".
- Een favicon in stijl (mag voorlopig een eenvoudig gouden roosje of monogram als SVG zijn dat je zelf genereert, plekhouder toegestaan).
- `lang="nl"` op het html-element.

## Structuur, van boven naar beneden

### 1. Hero (schermvullend op telefoon)

- Achtergrond: `beelden/splash.jpg` (zie Beschikbaar beeldmateriaal). Geen plekhouder, dit beeld is definitief.
- Daarop de titel "De Rozen van Zilverweide" (Cinzel) en daaronder de heldenzin (zie teksten).
- Geen menubalk, geen navigatie, geen logo-balk.

### 2. De film

- Eén videospeler met een groot posterbeeld en een duidelijke play-knop. Geluid gaat aan bij handmatig starten. Geen autoplay.
- De video mag pas beginnen te laden wanneer de bezoeker op play drukt (`preload="none"` plus posterbeeld). Tot dat moment kost de film de bezoeker geen data.
- Plekhouders: `[Placeholder: cinematic film, mp4]` voor de videobron en `[Placeholder: posterbeeld cinematic]` voor het posterbeeld.
- Bouw dit zo dat later alleen de video- en posterbron vervangen hoeven te worden, zonder structuurwijziging.

### 3. Verhaalblok

- Kort tekstblok in perkamentkleur op de donkere achtergrond. Teksten hieronder letterlijk overnemen.

### 4. Sfeerbeelden

- Drie of vier beelden als flarden van de wereld, geen uitleg van spelmechanieken.
- Eerste beeld: `beelden/heks.jpg` (definitief). De overige twee of drie als plekhouders: `[Placeholder: sfeerbeeld 2]` tot en met `[Placeholder: sfeerbeeld 4]`.
- De aangeleverde beelden zijn liggend (het spel is landscape). Toon op een staande telefoon per beeld een automatisch bijgesneden, staande of vierkante uitsnede (`object-fit: cover`), en op bredere schermen meer van het volledige beeld.
- Maak per beeld het middelpunt van de uitsnede instelbaar met één duidelijke waarde per afbeelding (`object-position`), met een kort commentaar in de code dat uitlegt hoe ik dat per beeld aanpas.

### 5. Afsluiting met acties

- Primair: één duidelijke knop "Volg op Instagram", link nu als plekhouder `[Placeholder: instagram-url]`. Daaronder het volgzinnetje (zie teksten).
- Secundair en visueel kleiner: het playtestzinnetje (zie teksten) met een maillink. Gebruik een mailto-link met plekhouder `[Placeholder: mailadres]` en een voorgevuld onderwerp "Aanmelding playtest Zilverweide".
- Helemaal onderaan een minimale regel: "De Rozen van Zilverweide is een productie van Calovia."

## Teksten (letterlijk overnemen, niets bijschrijven)

**Heldenzin onder de titel:**

> Een speelbaar mysterie. Samen zoeken jullie de waarheid van een dorp dat zijn geheimen liever bewaart.

**Verhaalblok:**

> Lang geleden brandde in Zilverweide een molen tot de grond toe af. Een ongeluk, zei men. Maar er zijn namen die sindsdien niemand meer hardop uitspreekt.
>
> De Rozen van Zilverweide is een coöperatief mysterie dat je met je groep op locatie speelt. Ieder krijgt een eigen rol, een eigen scherm en een eigen stukje van de waarheid. Alleen samen leggen jullie bloot wat er die nacht werkelijk gebeurde.
>
> Binnenkort speelbaar.

**Volgzinnetje onder de Instagram-knop:**

> Volg ons en hoor als eerste wanneer het dorp zijn poorten opent.

**Playtestzinnetje:**

> Eerder meespelen? Deze zomer spelen de eerste groepen. Stuur een berichtje en test het mysterie als een van de eersten.

**Omschrijving voor het linkvoorbeeld (meta description en Open Graph):**

> Een speelbaar mysterie op locatie. Ieder een eigen rol, samen één waarheid. Binnenkort speelbaar.

## Wat er NIET op mag

- Geen menu, geen navigatie, geen meerdere pagina's.
- Geen prijzen, geen speeldata, geen boekingsformulier, geen aftelklok.
- Geen tweede video.
- Geen nieuwsbriefformulier, geen andere social-knoppen dan Instagram.
- Geen cookiebanner, geen analytics, geen trackers, geen externe ingesloten spelers (geen YouTube of Vimeo).
- Geen scroll-hijacking, geen zware parallax, geen deeltjeseffecten. Subtiele, rustige overgangen mogen (bijvoorbeeld een zachte fade bij het laden van de hero), meer niet.
- Geen extra secties, teksten of features die niet in deze opdracht staan. Eenvoud is een eis, geen gebrek.

## Tekstregels (strikt)

- Alle zichtbare tekst in het Nederlands.
- Nooit em-dashes (lange gedachtestreepjes) in zichtbare tekst. Gebruik komma's, gewone haakjes of herschrijf de zin.
- Toon: sfeervol en terughoudend, geen marketingtaal, geen uitroeptekens.

## Plekhouders

Alle plekhouders vormgeven als nette, gestileerde donkere vlakken met de plekhoudertekst in gedimd goud, zodat de pagina er ook zonder definitief beeldmateriaal verzorgd uitziet. Elke plekhouder moet vervangbaar zijn door alleen een bron of link te wijzigen.

## Oplevering en publicatie (GitHub Pages)

- Deze site leeft in een eigen, aparte, publieke repository (los van de game-repo). De huidige werkmap is die repo. Plaats `index.html` in de root, beelden in `beelden/`.
- Voeg een `CNAME` bestand toe met inhoud `zilverweide.nl`.
- Lever een kort stappenlijstje mee (als `PUBLICEREN.md`) met daarin: hoe ik GitHub Pages aanzet voor deze repo, hoe ik eerst test op het gratis github.io-adres voordat het domein gekoppeld is, welke DNS-instellingen ik daarna bij de domeinprovider moet zetten (A-records en CNAME voor www), en hoe ik controleer dat het werkt, inclusief het aanzetten van HTTPS.
- Bovenin `index.html` een kort commentaarblok met een lijstje: welke plekhouders er zijn en hoe ik ze vervang.
- Test het resultaat visueel op een smal scherm (circa 380 pixels breed) en op desktop.

## Instructie voor mijzelf (niet voor de bouwer, ter herinnering)

- Nieuwe publieke repo aanmaken (bijvoorbeeld `zilverweide-site`), los van de game-repo. Dit opdrachtbestand erin zetten, plus `beelden/splash.jpg` en `beelden/heks.jpg`. Claude Code starten in die map.
- De cinematic apart exporteren als webversie: mp4 (H.264), 1080p is genoeg, mikken op ongeveer 15 tot 25 MB. Niet de volle-kwaliteit-export op de site zetten.
- Domein zilverweide.nl registreren en mail-doorsturen aanzetten (bijvoorbeeld speel@zilverweide.nl naar eigen mailbox).
- Instagram-account aanmaken en minimaal drie posts plaatsen voordat de link op de site ingevuld wordt.
