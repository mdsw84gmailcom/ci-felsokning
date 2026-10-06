# Fellogg

En rad per fel. Skriv medan du minns hur du gjorde.

| Nr | Vad stod i loggen? | Lokalt eller på GitHub? | Hur tog du reda på orsaken? | Hur löste du det? |
|----|--------------------|-------------------------|-----------------------------|-------------------|
| 1  | Github actions visade att det var fel i yaml-syntaxen | Github | Jag öppnade `ci.yml` och såg att intenderingen var fel | Jag rättade indraget så att steget låg på samma nivå som dem andra stegen |
| 2  | Hittar inte lockfile i uv.lock | Lokalt | Jag körde samma kommando lokalt som i workflow och såg att uv förväntade sig en lockfil. | Skapa en `uv.lock` med uv lock |
| 3  | Ruff rapporterar F401 för att os importerades i `baseline.py` men användes aldrig. | Lokalt | Körde nästa kommandot i workflow `uv run ruff check src tests` | Tog bort den oandvända importen |
| 4  | Ruff rapporterade att `tests/test_baseline.py` inte följer formateringsreglerna. | Lokalt |  Körde kommandot efter i workflow `uv run ruff format --check src tests` | Lät Ruff fixa det automatiskt med `uv run format tests/test_baseline.py` |
| 5  | Pytest misslyckades pga `ModuleNotFoundError` för att numpy fanns inte med. | Lokalt | Körde kommandot efter i workflow `uv run pytest` | Kollade i `features.py` och såg att numpy importerades där sen gick jag in i `pyproject.toml` och såg att den inte fanns med så jag lade till numpy som dependency och uppdaterade uv.lock |
| 6  | Pytest misslyckades, visade fel värden från moving_average | Lokalt | Körde kommandot efter i workflow uv run pytest  | Jag kollade i features.py på funktionen moving_average och såg att kernel delades med window +1 istället för window. Ändrade det till window så medelvärdet räknas korrekt. |
| 7  |                    |                         |                             |                   |
| 8  |                    |                         |                             |                   |
| 9  |                    |                         |                             |                   |

Fortsätt tabellen med fler rader vid behov.
