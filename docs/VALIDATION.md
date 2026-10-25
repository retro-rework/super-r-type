# Validation — Super R-Type Retro Rework v1.0 (paquet cumulatif)

Date : 2026-10-25. Vérifications faites sur des copies, sans modifier ORIGINAL, STABLE ni la build v1.0.

## Patch
- `Super-R-Type-Retro-Rework-v1.0.bps` : **36 894 octets**, SHA-256 `27f6144674b12d2a97a4f51232e93ed1ce2659c4cae6967cbff88dce1ab5ff02`.
- Contenu : SA-1 Root v1.3 (USA) de Vitor Vilela et les modifications Retro Rework (respawn, Stage Select au menu principal).
- Généré par `RELEASE_PREP/tools/make_release.js` avec `release_super-r-type_v1.0.json`. La génération est déterministe.

| | Fichier | SHA-256 | CRC32 |
|---|---|---|---|
| Entrée | Super R-Type (USA), originale | `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b` | `8B22C830` |
| Sortie | Super R-Type Retro Rework v1.0 | `0a5b3a784a0cceffeaf954812235341c8d3bb93b304158547ebb8347ab14257e` | `36CBF8CA` |

## Résultats
| Vérification | Résultat |
|---|---|
| Patch appliqué à la ROM USA originale (installation en une étape) | **SHA-256 identique à la build v1.0 validée** |
| `CHECKSUMS.sha256` (patch, entrée, sortie) | 3/3 conformes |
| ROM source après application | inchangée (SHA-256 identique) |
| ROM déjà patchée SA-1 Root (`292f295d…`) | refusée (CRC source), aucun fichier produit |
| Build STABLE (respawn seul) | refusée |
| ROM USA avec en-tête de 512 octets | refusée |
| Lancement de la ROM obtenue dans Mesen 2.2.1 | titre avec `< STAGE 1 >` ; STAGE 3 choisi et lancé, conditions standard |
| Tests fonctionnels de la build v1.0 (`AI REPORTS/2026-10-25_Claude_StageSelect_v01_Resultats.md`) | conformes, inchangés : même build |

## Limites
- **Application vérifiée avec l'outil BPS de Retro Rework** (`RELEASE_PREP/tools/bps.js`), validé sur le patch BPS officiel de SA-1 Root. Les outils tiers (Flips, Rom Patcher JS, beat) n'ont pas été essayés ici.
- Validation logicielle sous Mesen 2.2.1. bsnes et Snes9x ne sont pas testés.
- Le 25 octobre 2026, j'ai effectué un **test rapide concluant sur ma Super Nintendo réelle**. Ce résultat est mon retour de test manuel, distinct des vérifications de Claude ci-dessus. Il ne constitue pas une validation exhaustive de toutes les configurations matérielles (modèles de consoles, cartouches ou adaptateurs).
- On October 25, 2026, I performed a **successful quick test on my real Super Nintendo**. This is my reported manual hardware test, separate from Claude's checks above, not exhaustive validation of every hardware configuration. bsnes and Snes9x remain untested.
- Seule la version USA est prise en charge.
- **Droits** : le dépôt SA-1 Root ne publie pas de licence. Ce patch redistribue le travail de Vitor Vilela, crédité dans `CREDITS.md`. La distribution cumulative a été décidée par l'équipe Retro Rework ; une autorisation de l'auteur est recommandée avant toute publication publique.
