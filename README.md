# WoW Quest Journal

A World of Warcraft-inspired quest journal built as a lightweight static web application.

## Features

- Loads quests from a remote AWS API endpoint
- Presents active and completed quest lists
- Supports completing and restoring quests in the browser
- Includes local JSON data and multiple interface experiments
- Runs without a frontend build tool

## Run locally

Because the application loads JSON and calls an external API, serve it over HTTP rather than opening the file directly:

```bash
python -m http.server 8000
```

Open one of the available interfaces:

- [http://localhost:8000/quest-log.html](http://localhost:8000/quest-log.html)
- [http://localhost:8000/wow_quest_journal_ui.html](http://localhost:8000/wow_quest_journal_ui.html)

## Repository layout

```text
.
├── quest-log.html
├── wow_quest_journal_ui.html
├── quests.json
└── saves/
```

## Notes

The live experience depends on the configured API endpoint remaining available and allowing browser requests from the local or deployed origin. For a production release, move the endpoint into configuration and add error, loading, and offline states.
