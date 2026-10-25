# Validation — Super R-Type Retro Rework v1.0 (paquet de distribution)

Date : 2026-10-25. Vérifications faites sur des copies, sans modifier ORIGINAL ni STABLE.

## Chaîne de reconstruction
| Étape | Fichier | SHA-256 | CRC32 |
|---|---|---|---|
| ROM du joueur | Super R-Type (USA) | `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b` | `8B22C830` |
| + SA-1 Root v1.3 (USA, Vitor Vilela) | ROM SA-1 | `292f295d44d0569a7954151ab74b28845361df1e5c12edbe4f519da14e18a892` | `0D73E7D3` |
| + `Super-R-Type-Retro-Rework-v1.0.bps` | **Retro Rework v1.0** | `0a5b3a784a0cceffeaf954812235341c8d3bb93b304158547ebb8347ab14257e` | `36CBF8CA` |

Patch distribué : `Super-R-Type-Retro-Rework-v1.0.bps`, 1 078 octets, SHA-256 `aecba31ee87182ec6500467773510a5533b4ca7b2c6400f94141300f7034c825`.

## Résultats
| Vérification | Résultat |
|---|---|
| Empreintes avant/après SA-1 Root comparées à celles publiées par Vitor Vilela (README SA-1 Root) | identiques |
| Patch SA-1 Root (dépôt officiel, `Super-R-Type/patch.bps`) appliqué à la ROM USA | ROM SA-1 identique (SHA-256) |
| Patch Retro Rework appliqué à la ROM SA-1 | **identique à la build v1.0 retenue (SHA-256)** |
| Patch Retro Rework appliqué directement à la ROM USA (étape 1 oubliée) | refusé (CRC source), aucun fichier produit |
| Lancement dans Mesen 2.2.1 de la ROM reconstruite | écran titre avec `< STAGE 1 >`, sélection STAGE 3, départ au stage 3 avec les conditions standard |
| Tests fonctionnels de la build (rapport `AI REPORTS/2026-10-25_Claude_StageSelect_v01_Resultats.md`) | 7 stages, CONFIG, démo, Continue, fonctions cachées, respawn, performances SA-1 : conformes |

## Limites
- **Application vérifiée avec l'outil BPS de Retro Rework** (`RELEASE_PREP/tools/bps.js`), lui-même validé sur le patch officiel SA-1 Root. Les patchers tiers (Flips, Rom Patcher JS, beat) ne sont pas installés ici. Le format BPS standard est respecté, mais ces outils n'ont pas été essayés.
- Testé uniquement sous Mesen 2.2.1. bsnes, Snes9x et le matériel réel ne sont pas testés.
- Seule la version USA est prise en charge.
