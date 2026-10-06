# Fellogg

En rad per fel. Skriv medan du minns hur du gjorde.

| Nr | Vad stod i loggen? | Lokalt eller på GitHub? | Hur tog du reda på orsaken? | Hur löste du det? |
|----|--------------------|-------------------------|-----------------------------|-------------------|
| 1  | Github actions visade att det var fel i yaml-syntaxen | Github | Jag öppnade `ci.yaml` och såg att intenderingen var fel | Jag rättade indraget så att steget låg på samma nivå som dem andra stegen |
| 2  | Hittar inte lockfile i uv.lock | Lokalt | Jag körde samma kommando lokalt som i workflow och såg att uv förväntade sig en lockfil. | Skapa en `uv.lock` med uv lock |
| 3  | Ruff rapporterar F401 för att os importerades i `baseline.py` men användes aldrig. | Lokalt | Körde nästa kommandot i workflow `uv run ruff check src tests` | Tog bort den oandvända importen |
| 4  |                    |                         |                             |                   |
| 5  |                    |                         |                             |                   |
| 6  |                    |                         |                             |                   |
| 7  |                    |                         |                             |                   |
| 8  |                    |                         |                             |                   |
| 9  |                    |                         |                             |                   |

Fortsätt tabellen med fler rader vid behov.
