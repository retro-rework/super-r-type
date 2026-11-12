# Validation — Super R-Type Retro Rework v1.1 (paquet cumulatif)

Date : 2026-11-10. Vérifications faites sur des copies, sans modifier ORIGINAL, STABLE ni les builds validées.

## Patch
- `Super-R-Type-Retro-Rework-v1.1.bps` : **37 270 octets**. Le SHA-256 figure dans `CHECKSUMS.sha256`.
- Contenu : SA-1 Root v1.3 (USA) de Vitor Vilela, plus les modifications Retro Rework (respawn, Stage Select, record sauvegardé, HI-SCORE sur le titre).
- Généré par `RELEASE_PREP/tools/make_release.js` avec `release_super-r-type_v1.1.json`.

| | Fichier | SHA-256 | CRC32 |
|---|---|---|---|
| Entrée | Super R-Type (USA), originale | `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b` | `8B22C830` |
| Sortie | Super R-Type Retro Rework v1.1 | `c3a02dfdd5ea37f5a3b77684c91cc57a3e8d1d76b11011f8fcdda89853d4707d` | `1FE560DD` |

## Résultats
- **Application du patch :** sur la ROM USA, la sortie est identique à la build validée par le créateur, avec `bps.js` comme avec RomPatcher.js (le moteur du patcheur en ligne).
- **Sauvegarde, 4 scénarios :** vierge, record conservé (12 300 affiché sur le titre et sur CONTINUE), sauvegarde corrompue ignorée, record battu sauvegardé.
- **7 stages, 6 000 images chacun :** le jeu n'écrit jamais dans la zone de sauvegarde (`$40:7E00-$7FFF`).
- **CONFIG :** la ligne HI-SCORE est masquée puis réaffichée.
- **Persistance :** Mesen recharge le record depuis son `.srm`.
- **Validation créateur :** build acceptée le 2026-11-10.
- **Rapport :** `AI REPORTS/2026-11-10_Claude_HiScore_Sauvegarde.md`.

## Limites
- Testé sous Mesen, et par le créateur sur Super Nintendo réelle avec SD2SNES. bsnes, Snes9x et les autres cartouches flash ne sont pas testés.
- SD2SNES (complément du 2026-11-12) : avec un firmware modifié (sd2snes+ 2.16.1) et « In-game hook » activé, une bande du décor du stage 1 apparaît décalée. Le défaut existe aussi avec les ROM USA et JP d'origine, et disparaît quand l'option est désactivée. D'après son auteur, le firmware officiel à jour corrige ce cas.
- Seule la version USA est prise en charge.
- **Droits :** comme pour la v1.0, ce patch redistribue le travail SA-1 Root de Vitor Vilela, crédité dans `CREDITS.md`.
