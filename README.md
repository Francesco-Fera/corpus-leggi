# corpus-leggi

Corpus Markdown delle leggi italiane, aggiornato automaticamente da [Normattiva](https://www.normattiva.it) (IPZS).

## Stato

🚧 **Work in progress.** Il dataset è in fase di popolamento iniziale. La pipeline di ingestion è sviluppata in [corpus-leggi-tools](https://github.com/Francesco-Fera/corpus-leggi-tools).

## Formato

Un file Markdown **per articolo**, organizzato per tipo di atto e anno:

```
leggi/
├── costituzione/
│   ├── _index.md
│   └── art-1.md ... art-139.md
├── codici/
│   └── codice-amministrazione-digitale/
│       ├── _index.md
│       └── art-1.md ...
└── legge/
    └── 2024/
        └── legge_20241213_203/
            ├── _index.md
            ├── art-1.md
            └── ...
```

Ogni file ha front matter YAML con metadati (`atto`, `articolo`, `urn`, `vigente`, `aggiornato_al`, ecc.) e corpo Markdown pulito adatto a LLM/RAG.

## Aggiornamento

- **Daily** 07:00 UTC — sync degli atti modificati nelle 24h precedenti.
- **Weekly** domenica 02:00 UTC — resync per catturare slippage.
- La storia git rappresenta la **timeline normativa**: `git blame art-5.md` mostra quando ogni comma è stato introdotto o modificato.

## Attribuzione

**Fonte:** [Normattiva](https://www.normattiva.it) — Istituto Poligrafico e Zecca dello Stato (IPZS).

I dati Normattiva sono rilasciati sotto [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.it) dal 1° gennaio 2026 ([comunicato ufficiale IPZS](https://www.ipzs.it/allegati/docs/1771941018709_COMUNICATOSTAMPANORMATTIVAOK.pdf)).

## Disclaimer

⚠️ I testi in questo repository **non hanno carattere di ufficialità**. L'unico testo ufficiale è quello pubblicato sulla [Gazzetta Ufficiale](https://www.gazzettaufficiale.it). Vedi [DISCLAIMER.md](DISCLAIMER.md).

## Licenza

Dataset: [CC BY 4.0](LICENSE) — puoi riusarlo liberamente, anche commercialmente, con attribuzione.
