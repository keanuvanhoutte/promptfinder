# PromptFinder

Persoonlijke app om commando's en begrippen uit screenshots en lesslides (PowerPoint) te halen, uit te leggen en per tab (Algemeen, Linux, HTML, PyMOL …) doorzoekbaar te bewaren.

De app zelf draait als artifact op claude.ai. Deze repository is de **reservekopie** (broncode + back-up van alle data) én de **openbare leesversie**.

## Online bekijken (zonder Claude)

**https://keanuvanhoutte.github.io/promptfinder/**

Iedereen met deze link kan de lijst doorzoeken, zonder account. Het is alleen lezen: toevoegen en screenshots laten uitleggen kan enkel in de Claude-versie.
De pagina leest `backup/promptfinder-backup.json`. Wordt die back-up hier vernieuwd, dan toont de link binnen enkele minuten de nieuwe lijst.

## Inhoud

| Map / bestand | Wat |
|---|---|
| `index.html` | De openbare leesversie (GitHub Pages). |
| `app/index.html` | Broncode van de app (zoals gepubliceerd op claude.ai). |
| `app/promptfinder-default.html` | Losse leesversie om door te sturen (momentopname, werkt zonder internet). |
| `app/eng-traineddata.gz.b64.txt` | Taalbestand voor de lokale tekstherkenning (reserve als Claude niet beschikbaar is). |
| `backup/promptfinder-backup.json` | Volledige back-up van alle tabs en prompts. Terug te zetten in de app. |
| `backup/prompts-leesbaar.md` | Dezelfde data als leesbare lijst, handig om op GitHub te bekijken. |

Niet in deze back-up: de bewaarde screenshots zelf (de afbeeldingen achter "Bekijk screenshot"). De tekst van elk voorbeeld (commando, uitvoer, uitleg) zit wel in de JSON.

## Data terugzetten

1. Open PromptFinder.
2. Menu **⋯** → **Back-up terugzetten…**
3. Kies `backup/promptfinder-backup.json` (eerst downloaden van GitHub).

Wat in de back-up staat wordt teruggezet. Wat er nu in de app staat en niet in de back-up, blijft staan.

## Back-up bijwerken

1. In de app: menu **⋯** → **Back-up downloaden (.json)**.
2. Op GitHub: open de map `backup` → **Add file** → **Upload files** → sleep het nieuwe bestand erin → **Commit changes**. Het bestand moet exact `promptfinder-backup.json` heten, anders ziet de openbare link het niet.

Zo heb je op GitHub ook de geschiedenis van al je vorige back-ups.
