# EZ Shows — publiek

Lege hulzen voor het werk op tour. Pagina's die op zichzelf niets zeggen en pas
betekenis krijgen op het moment dat er een link van gemaakt wordt.

## De regel

> **Alles wat hier in staat is wereldwijd te lezen. Voor altijd, en ook de
> geschiedenis — iets weghalen uit een latere versie haalt het niet uit git.**

Hier komt dus nooit in: een prijslijst met inkoopprijzen, een telefoonnummer, een
contactpersoon, een adres. Dat hoort in de privé-repo `tumbi`.

Twijfel je? Dan hoort het er niet in.

### Eén uitzondering, en die is bewust gemaakt

In `t/` staan korte links naar een telling, en **die dragen de show wél in zich**:
artiest, zaal, datum en de voorraad van die stand. Dat is een afweging, geen
slordigheid.

De lange links droegen alles achter de `#`, en dat bereikte de server nooit. Maar
het waren zevenhonderd tekens, en WhatsApp knipt zo'n reeks soms af — de teller
krijgt dan een halve link en er gaat niets open. Dat is in de praktijk gebeurd.
Een korte link kan niet afgeknipt worden, en daarvoor moet de show ergens staan.

Elke map in `t/` heeft een willekeurig staartje (`...-k3f9`) zodat het adres niet
te raden is. **Dat is verstopping, geen slot.** Wie het adres heeft kan de
telling van die stand zien. Er staat daarom niets anders in dan wat er geteld
moet worden: geen prijzen, geen omzet, geen namen van mensen.

Hoort een show echt niet op het open web, gebruik dan de lange link — die blijft
gewoon werken.

## Hoe de showgegevens dan wél bij de pagina komen

Achter de `#` van de link. Een browser stuurt dat stuk **nooit** naar de server
waar de pagina staat — het blijft tussen de twee telefoons die het bericht
delen. GitHub ziet alleen dat er iemand `standcount/` heeft opgehaald, nooit welke
show.

Daarom staat er in dit bestand nergens iets over een show, en hoort dat zo te
blijven.

## Wat er nu in staat

| Map | Wat het is |
|---|---|
| `standcount/` | **Stand Count** — het telvel voor een standteller. Opent met één tik vanuit WhatsApp, ook op een iPhone — waar een `.html`-bijlage juist niet opengaat. |
| `t/` | Korte links per show. Elk mapje stuurt door naar `standcount/` met die show erachter. Gemaakt door `web/kortelink.py` in de privé-repo. |

## Waar de bron staat

Niet hier. De bron van `standcount/index.html` is
`02-werk/tumbi/web/standcount.html`, in de privé-repo, naast de tool die de links
maakt. Deze repo is alleen de etalage.

Bijwerken gaat met één opdracht, vanuit de tumbi-map:

```bash
./web/publiceer.sh
```

Die kopieert, commit en pusht. Doe het niet met de hand — twee kopieën die uit
elkaar lopen is precies hoe je op een avond in de zaal ontdekt dat de teller een
oude versie heeft.
