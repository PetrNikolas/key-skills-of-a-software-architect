## Cíl
Vytvořit neutrální `PROJECT_CONTEXT.md` s plnou analýzou projektu a propojit ho referencemi ze stávajících konfiguračních souborů (Claude, Gemini, Codex), aby každý AI nástroj věděl, kde najít kompletní kontext projektu.

## Krok 1 — Vytvořit `PROJECT_CONTEXT.md` v rootu
Nový soubor v češtině (konzistentní s projektem), strukturovaný do sekcí:

- **Účel projektu** — kurátorovaný plochý seznam klíčových dovedností/principů pro softwarové architekty
- **Obsah** — 21 položek v `README.md`, formát `- 💚 <princip> - <vysvětlení>.`
- **Struktura repozitáře** — přehled souborů a adresářů (README.md, AGENTS/CLAUDE/GEMINI.md, .claude/.codex/.gemini/, LICENSE, .gitignore, .idea/)
- **Konvence pro příspěvky** — přesná formátovací pravidla:
  - Pouze čeština s diakritikou
  - Plochý seznam (žádné kategorie/podsekce)
  - Formát `- 💚 <princip> - <vysvětlení>.`
  - Žádný kód, žádné rich formatting (bold/italics/links)
  - Jednotlivá položka = jeden princip + krátké vysvětlení
- **Technický kontext** — žádný build systém, žádné závislosti, čistě dokumentační repozitář, MIT licence, GitHub remote
- **Git kontext** — větev `main`, remote `github.com/PetrNikolas/key-skills-of-a-software-architect`

## Krok 2 — Přidat reference do existujících Markdown configů
Na konec každého z těchto souborů přidat jeden řádek odkazující na `PROJECT_CONTEXT.md`:
- `AGENTS.md`
- `CLAUDE.md`
- `GEMINI.md`

Forma (česky, konzistentní se stylem): `Kompletní kontext projektu najdete v souboru [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md).`

## Krok 3 — Přidat reference do konfiguračních JSON/TOML
- `.claude/settings.json` — přidat pole `"_context": "Kompletní kontext projektu v PROJECT_CONTEXT.md"` (zachová styl `_comment`)
- `.gemini/settings.json` — analogicky
- `.codex/config.toml` — přidat řádek komentáře `# Kompletní kontext projektu najdete v PROJECT_CONTEXT.md.` (zachová styl komentáře)

## Co se NIKDY nezmění
- `README.md` a jeho 21 položek (žádná úprava obsahu)
- Struktura projektu
- Licence, .gitignore, .idea/

## Ověření
Po implementaci zkontroluji, že:
- `PROJECT_CONTEXT.md` existuje a obsahuje všechny sekce
- Všechny 3 `.md` configy obsahují referenci
- Všechny 3 skryté configy obsahují referenci
- `README.md` je netknutý