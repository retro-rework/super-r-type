> **Archive antérieure au test sur console réelle.** Pour l’état actuel : le 25 octobre 2026, j’ai effectué un test rapide concluant sur ma SNES réelle, sans validation exhaustive des configurations. Voir [la validation actuelle](VALIDATION.md). / **Archive predating the real-hardware test.** I performed a successful quick test on my real SNES on October 25, 2026, without exhaustive hardware validation. See [the current validation](VALIDATION.md).

> Archive du paquet incrémental reçu : installation en deux étapes. Ce document ne décrit pas le futur patch cumulatif. / Archive of the supplied add-on package: two-step installation, not the planned cumulative patch.

# Super R-Type — Retro Rework v1.0

*[Français](#français) · [English](#english)*

---

## Français

**Super R-Type Retro Rework** est un patch pour Super R-Type (Super Nintendo, Irem, 1991). Il s'applique par-dessus l'accélération **SA-1 Root** de Vitor Vilela, qui supprime les ralentissements du jeu d'origine.

Il ajoute :
- **un respawn sur place** : après une perte de vie, le vaisseau réapparaît là où il a été détruit, sans retour au point de contrôle ;
- **un Stage Select dans le menu principal** : `< STAGE 1 >` à `< STAGE 7 >`, réglable avec Gauche/Droite sur l'écran titre.

Le détail est dans [CHANGELOG.md](../CHANGELOG.md).

> Aucune ROM n'est fournie. Vous devez posséder la cartouche originale de Super R-Type et en extraire votre propre copie.

### Ce qu'il vous faut
1. **Votre ROM Super R-Type (USA)**, sans en-tête (1 048 576 octets) :
   - SHA-256 `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b`
   - CRC32 `8B22C830`
2. **Le patch SA-1 Root de Super R-Type, version USA (v1.3)**, à télécharger chez son auteur :
   https://github.com/VitorVilela7/SA1-Root/releases
   (onglet *Releases*, fichier BPS de Super R-Type pour la version américaine).
3. **Le patch Retro Rework** de ce dossier : `Super-R-Type-Retro-Rework-v1.0.bps`.
4. **Un outil d'application de patch BPS**, par exemple :
   - [Flips](https://sneslab.net/tools/floating.zip) ;
   - [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) (dans le navigateur) ;
   - [beat](https://www.romhacking.net/utilities/893/).

### Installation (2 étapes)
1. **Appliquez le patch SA-1 Root** à votre ROM USA. Le résultat doit avoir le SHA-256
   `292f295d44d0569a7954151ab74b28845361df1e5c12edbe4f519da14e18a892` (CRC32 `0D73E7D3`).
2. **Appliquez `Super-R-Type-Retro-Rework-v1.0.bps`** à cette ROM SA-1. Le résultat doit avoir le SHA-256
   `0a5b3a784a0cceffeaf954812235341c8d3bb93b304158547ebb8347ab14257e` (CRC32 `36CBF8CA`).

Les empreintes sont reprises dans [CHECKSUMS.sha256](CHECKSUMS-SOURCE.sha256). Le format BPS contrôle la ROM d'entrée : si l'outil refuse le patch, la ROM n'est pas la bonne (mauvaise région, en-tête de 512 octets, ou étape 1 non effectuée).

### Jouer
- **Écran titre** : Gauche/Droite pour choisir le stage, Start pour jouer, Select pour CONFIG (inchangé).
- **Émulateurs** : validé sous **Mesen 2.2.1**. SA-1 Root est annoncé compatible avec bsnes, Snes9x et le matériel réel (SD2SNES/FXPAK, cartouche SA-1). Ces derniers n'ont pas encore été testés avec Retro Rework.
- Le jeu requiert **32 Ko de BW-RAM** (en-tête SA-1 standard, géré par les émulateurs compatibles).
- **Non compatible** : versions européenne et japonaise (le patch Retro Rework est conçu pour la version USA), ZSNES.

---

## English

**Super R-Type Retro Rework** is a patch for Super R-Type (Super Nintendo, Irem, 1991). It applies on top of Vitor Vilela's **SA-1 Root** acceleration, which removes the original game's slowdown.

It adds:
- **on-the-spot respawn**: after losing a life, your ship reappears where it was destroyed instead of going back to the checkpoint;
- **a main-menu Stage Select**: `< STAGE 1 >` to `< STAGE 7 >`, changed with Left/Right on the title screen.

See [CHANGELOG.md](../CHANGELOG.md) for details.

> No ROM is provided. You must own an original Super R-Type cartridge and dump your own copy.

### Requirements
1. **Your Super R-Type (USA) ROM**, unheadered (1,048,576 bytes):
   - SHA-256 `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b`
   - CRC32 `8B22C830`
2. **The SA-1 Root patch for Super R-Type, USA version (v1.3)**, downloaded from its author:
   https://github.com/VitorVilela7/SA1-Root/releases
   (*Releases* tab, Super R-Type BPS for the American version).
3. **The Retro Rework patch** in this folder: `Super-R-Type-Retro-Rework-v1.0.bps`.
4. **A BPS patching tool**, for example:
   - [Flips](https://sneslab.net/tools/floating.zip);
   - [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) (in your browser);
   - [beat](https://www.romhacking.net/utilities/893/).

### Installation (2 steps)
1. **Apply the SA-1 Root patch** to your USA ROM. The result must have SHA-256
   `292f295d44d0569a7954151ab74b28845361df1e5c12edbe4f519da14e18a892` (CRC32 `0D73E7D3`).
2. **Apply `Super-R-Type-Retro-Rework-v1.0.bps`** to that SA-1 ROM. The result must have SHA-256
   `0a5b3a784a0cceffeaf954812235341c8d3bb93b304158547ebb8347ab14257e` (CRC32 `36CBF8CA`).

Checksums are also listed in [CHECKSUMS.sha256](CHECKSUMS-SOURCE.sha256). BPS checks the input ROM: if your tool rejects the patch, the ROM is not the right one (wrong region, 512-byte header, or step 1 skipped).

### Playing
- **Title screen**: Left/Right to choose the stage, Start to play, Select for CONFIG (unchanged).
- **Emulators**: validated on **Mesen 2.2.1**. SA-1 Root is stated to work on bsnes, Snes9x and real hardware (SD2SNES/FXPAK, SA-1 cartridge); these have not been tested with Retro Rework yet.
- The game requires **32 KB of BW-RAM** (standard SA-1 header, handled by compatible emulators).
- **Not compatible**: European and Japanese versions (the Retro Rework patch targets the USA version), ZSNES.

---

Super R-Type © 1991 Irem. Retro Rework is a non-commercial fan project, not affiliated with or endorsed by Irem, its successors or Nintendo. See [CREDITS.md](../CREDITS.md).
