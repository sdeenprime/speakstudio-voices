# SpeakStudio Voices

Voice library pulled from Google Drive (SpeakStudio → Voices) and reorganised for easy browsing.
**119 samples · ≈50 MB**

Old `Premium/` and `Regular/` folders are gone. Everything is grouped by **who the voice is**, not by tier:

```
speakstudio-voices/
├── male/        65 voices — English-language male voices (US, UK, Australian, South African)
├── female/      26 voices — English-language female voices
├── nigerian/    15 voices — Nigerian voices (male & female together)
├── foreign/     13 voices — non-English accents (Arabic, German, French, Portuguese, Russian)
└── manifest.csv      every file with category, gender, accent, size and review flag
```

Rule applied: English and Nigerian voices are **not** foreign. `foreign/` only holds samples whose accent
is not English — Arabic, German, French, Portuguese, Russian.

## Breakdown

| Category | Total | Gender known | Needs review |
|---|---|---|---|
| `male/` | 65 | 59 male · 6 unknown | 6 |
| `female/` | 26 | 26 female | 3 |
| `nigerian/` | 15 | 10 male · 4 female · 1 unknown | 9 |
| `foreign/` | 13 | 10 male · 2 female · 1 unknown | 5 |
| **All** | **119** | | **23** |

## Highlights per folder

- **male/** — narrators & characters: Jack Bass (gritty storyteller), Clyde (vintage radio), Countdown Casey (radio DJ), Darrick Wilson, The Pharaoh 4, Wise Old Man, Tibrus Quickfoot, Carter (mystery), Jude (British podcaster), Lee (Australian), Kim, Trevor Noah, Tim Ferriss, Oz Pearlman.
- **female/** — Eliza, Ivy, Hope, Gigi, Charlotte, Janice, Victoria, Rhea, Seer Morganna, Cruella, Female Newscaster, plus TED/TEDx clips (Nadine Burke Harris ×2, Sonja Lyubomirsky, Sara Beery, Kasley Killam).
- **nigerian/** — Jamaldeen, Niyi Adelekan, Olaniyi Victor, Elrufai, Manasseh Mashi, Leo O Anifowose, Nimi Meta, Tanga Wanda, Ayomide FM NG, Dayo NG, olabisi FM NG, ololade, Flourish NG, Manaseh, My Voice.
- **foreign/** — Arabic (Arab knight, Arabic 3, Rayyan, Sofian, Naseer, Sari), German (helmut, jonarsch, michheaal), French (Lison), Portuguese (Marcus), Russian (Stanislav), Spanish/Portuguese (Carlos).

## 23 files flagged for your ear

Gender/accent was inferred from names where the file name didn't say. These need a quick listen — the `needs_review` column in `manifest.csv` marks them:

`male/`: Expressive Narrator, jsaccd, Sage, Surrey, theeconomist, Unknown Speaker
`female/`: Cass, Ember, Noushin
`nigerian/`: Ayomide FM NG, Dayo NG, Flourish NG, Leo O Anifowose, Manaseh, My Voice, Nimi Meta, olabisi FM NG, Tanga Wanda
`foreign/`: Arab knight, Arabic 3, Carlos, Naseer, Sari

To fix one, move the file and edit its row in `manifest.csv` — or open an issue with the filename and the correction.

## Adding a new voice

1. Drop the file in the folder it belongs to (`male/`, `female/`, `nigerian/`, `foreign/`).
2. Add a row to `manifest.csv` (category, gender, language_accent, size_kb).
3. Keep the naming pattern `<Name> - <Style/Use>.mp3` — it's how the library stays searchable.

## Provenance & usage

These are reference clips used for voice design in SpeakStudio. Some are cloned or captured voices of real people
(Trevor Noah, Tim Ferriss, Jefferson Fisher, Oz Pearlman, TED/TEDx speakers) and fictional characters
(Frank Underwood, Oliver Queen, Cruella). **This repo is public** — before reusing anything commercially, check
that you have the rights to the underlying voice, and consider keeping the repo private if the library is
internal-only.
