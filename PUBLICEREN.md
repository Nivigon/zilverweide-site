# Publiceren op GitHub Pages

Kort stappenlijstje om de site live te zetten op zilverweide.nl.

## 1. GitHub Pages aanzetten

1. Ga op GitHub naar deze repository, dan **Settings** en in het linkermenu **Pages**.
2. Bij **Build and deployment**, kies bij *Source* voor **Deploy from a branch**.
3. Kies de branch waarop `index.html` staat (meestal `main`) en de map **/ (root)**. Klik op **Save**.
4. Na een minuut of twee staat de site online.

## 2. Eerst testen op het gratis github.io-adres

Let op: er staat een `CNAME`-bestand in de repository. Daardoor vult GitHub het veld *Custom domain* automatisch in en stuurt het github.io-adres door naar zilverweide.nl, wat pas werkt als de DNS is ingesteld. Zo test je toch eerst op het gratis adres:

1. Ga naar **Settings, Pages** en maak het veld **Custom domain** tijdelijk leeg (klik op *Remove*). GitHub verwijdert dan ook het `CNAME`-bestand uit de repository, dat is normaal.
2. Open `https://nivigon.github.io/zilverweide-site/` en controleer de site op je telefoon en op je computer.
3. Klaar met testen? Vul bij **Custom domain** weer `zilverweide.nl` in en klik op **Save**. GitHub zet het `CNAME`-bestand dan zelf terug.

Tip: het linkvoorbeeld (Open Graph-beeld) verwijst naar `https://zilverweide.nl/beelden/og.jpg` en klopt dus pas volledig zodra het domein gekoppeld is.

## 3. DNS instellen bij de domeinprovider

Log in bij de provider waar zilverweide.nl geregistreerd is en zet deze records:

**Voor het kale domein (zilverweide.nl), vier A-records:**

| Type | Naam | Waarde |
|------|------|--------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**Voor www.zilverweide.nl, één CNAME-record:**

| Type | Naam | Waarde |
|------|------|--------|
| CNAME | www | nivigon.github.io |

Verwijder eventuele oude A- of CNAME-records voor `@` en `www` die de provider standaard heeft klaargezet (bijvoorbeeld een parkeerpagina).

DNS-wijzigingen kunnen even duren, meestal binnen een uur, soms tot een dag.

## 4. Domein koppelen en HTTPS aanzetten

1. Ga naar **Settings, Pages** en controleer dat bij **Custom domain** `zilverweide.nl` staat. GitHub doet dan een DNS-controle, wacht tot daar een groen vinkje staat.
2. Zet het vinkje **Enforce HTTPS** aan. Als dat vinkje nog grijs is, wacht dan even: GitHub moet eerst een certificaat aanvragen, dat kan tot een uur duren nadat de DNS klopt.

## 5. Controleren dat alles werkt

1. Open `https://zilverweide.nl` in een privevenster: de site laadt en het slotje in de adresbalk is dicht.
2. Open `https://www.zilverweide.nl`: die stuurt door naar het kale domein.
3. Open `http://zilverweide.nl` (zonder s): die stuurt door naar https.
4. Stuur de link naar jezelf in WhatsApp en controleer het linkvoorbeeld: titel, omschrijving en het beeld van de heks. WhatsApp bewaart voorbeelden een tijdje, dus als je een oud voorbeeld ziet, plak de link dan met iets erachter (bijvoorbeeld `https://zilverweide.nl/?x=1`) om een vers voorbeeld te forceren.
