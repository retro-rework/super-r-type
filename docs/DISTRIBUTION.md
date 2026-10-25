# État de distribution / Distribution status

## Français

Je prépare un seul patch cumulatif. Sa réception et sa vérification restent nécessaires avant de proposer une installation en une opération.

Les documents [INSTALLATION-SOURCE.md](INSTALLATION-SOURCE.md) et [VALIDATION-SOURCE.md](VALIDATION-SOURCE.md) sont conservés comme traces du paquet reçu. Ils décrivent **deux étapes**, et ne constituent pas les instructions finales de la distribution cumulative. Les liens relatifs du document d'installation ont été adaptés à cette arborescence ; ses empreintes sont conservées dans CHECKSUMS-SOURCE.sha256.

### Contrôle du fichier reçu le 25 octobre 2026

- Nom : `Super-R-Type-Retro-Rework-v1.0.bps`.
- Taille : 1 078 octets ; signature BPS1.
- SHA-256 : `aecba31ee87182ec6500467773510a5533b4ca7b2c6400f94141300f7034c825`.
- CRC32 source inscrit dans le BPS : `0D73E7D3` (ROM déjà modifiée avec SA-1 Root).
- CRC32 cible inscrit dans le BPS : `36CBF8CA`.
- CRC32 de la ROM originale USA : `8B22C830`, différent de la source exigée.

Je ne présente donc pas ce fichier comme un patch cumulatif. Je conserve le rapport de validation d'origine, qui constate également le refus du patch sur la ROM originale.

Je n'ai modifié ni ROM ni code de jeu, et je n'ai recréé aucun patch. Le dossier prévu pour le dépôt contient uniquement des documents Markdown ; aucune ROM ni donnée personnelle n'y est incluse.

## English

I am preparing a single cumulative patch. I still need to receive and verify that file before providing a one-operation installation.

I preserve INSTALLATION-SOURCE.md and VALIDATION-SOURCE.md as records of the supplied package. They describe **two steps**, rather than final cumulative-patch instructions. I have adapted its relative installation-document links to this layout; its checksums are preserved in CHECKSUMS-SOURCE.sha256.

The supplied 1,078-byte BPS file has source CRC32 `0D73E7D3` (already SA-1-patched ROM), whereas the original USA ROM has CRC32 `8B22C830`. Its SHA-256 is `aecba31ee87182ec6500467773510a5533b4ca7b2c6400f94141300f7034c825`, and its target CRC32 is `36CBF8CA`.

I therefore do not present it as a cumulative patch. I have not modified any ROM or game code, or recreated a patch. The proposed repository contains Markdown documents only, with no ROM or personal data.
