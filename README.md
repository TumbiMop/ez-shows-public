# EZ Shows — publiek

Lege hulzen voor het werk op tour. Pagina's die op zichzelf niets zeggen en pas
betekenis krijgen op het moment dat er een link van gemaakt wordt.

## De regel

> **Alles wat hier in staat is wereldwijd te lezen. Voor altijd, en ook de
> geschiedenis — iets weghalen uit een latere versie haalt het niet uit git.**

Hier komt dus nooit in: een prijslijst, een voorraad, een artiest, een zaal, een
datum, een telefoonnummer, een contactpersoon, een bestandsnaam waar een klant in
staat. Dat hoort in de privé-repo `tumbi`.

Twijfel je? Dan hoort het er niet in.

## Hoe de showgegevens dan wél bij de pagina komen

Achter de `#` van de link. Een browser stuurt dat stuk **nooit** naar de server
waar de pagina staat — het blijft tussen de twee telefoons die het bericht
delen. GitHub ziet alleen dat er iemand `telvel/` heeft opgehaald, nooit welke
show.

Daarom staat er in dit bestand nergens iets over een show, en hoort dat zo te
blijven.

## Wat er nu in staat

| Map | Wat het is |
|---|---|
| `telvel/` | Het telvel voor een standteller. Opent met één tik vanuit WhatsApp, ook op een iPhone — waar een `.html`-bijlage juist niet opengaat. |

## Waar de bron staat

Niet hier. De bron van `telvel/index.html` is
`02-werk/tumbi/web/telvel.html`, in de privé-repo, naast de tool die de links
maakt. Deze repo is alleen de etalage.

Bijwerken gaat met één opdracht, vanuit de tumbi-map:

```bash
./web/publiceer.sh
```

Die kopieert, commit en pusht. Doe het niet met de hand — twee kopieën die uit
elkaar lopen is precies hoe je op een avond in de zaal ontdekt dat de teller een
oude versie heeft.
