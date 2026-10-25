# Super R-Type — Retro Rework v1.0

*[Français](#français) · [English](#english)*

---

## Français

Avec **Retro Rework**, je revisite Super R-Type (Super Nintendo, Irem, 1991). Je mène ce projet personnel avec l'aide d'outils d'intelligence artificielle.

Mon patch **inclut l'accélération SA-1 Root v1.3 de Vitor Vilela**, qui supprime les ralentissements du jeu d'origine. J'ajoute aussi :
- **un respawn sur place** : après une perte de vie, le vaisseau réapparaît là où il a été détruit, sans retour au point de contrôle ;
- **un Stage Select dans le menu principal** : `< STAGE 1 >` à `< STAGE 7 >`, réglable avec Gauche/Droite sur l'écran titre.

Le détail est dans [CHANGELOG.md](CHANGELOG.md).

> Aucune ROM n'est fournie. Vous devez posséder la cartouche originale de Super R-Type et en extraire votre propre copie.

### Ce qu'il vous faut
1. **Votre ROM Super R-Type (USA) originale**, sans en-tête (1 048 576 octets) :
   - SHA-256 `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b`
   - CRC32 `8B22C830`
2. **Mon patch cumulatif unique** : [Super-R-Type-Retro-Rework-v1.0.bps](patches/Super-R-Type-Retro-Rework-v1.0.bps) (ouvrir le fichier puis utiliser le bouton de téléchargement). SA-1 Root est déjà inclus ; ne l'appliquez pas séparément.
3. **Un outil d'application de patch BPS**, par exemple :
   - [Flips](https://sneslab.net/tools/floating.zip) ;
   - [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) (dans le navigateur) ;
   - [beat](https://www.romhacking.net/utilities/893/).

### Installation (une seule étape)
Appliquez `Super-R-Type-Retro-Rework-v1.0.bps` à votre ROM Super R-Type (USA) originale.

Le résultat doit avoir le SHA-256 `0a5b3a784a0cceffeaf954812235341c8d3bb93b304158547ebb8347ab14257e` (CRC32 `36CBF8CA`).

Le format BPS vérifie la ROM d'entrée. Si l'outil refuse le patch, la ROM n'est pas la bonne :
- version européenne ou japonaise ;
- en-tête de 512 octets (fichier de 1 049 088 octets) ;
- ROM déjà modifiée, par exemple déjà patchée avec SA-1 Root.

Les empreintes sont reprises dans [CHECKSUMS.sha256](CHECKSUMS.sha256).

### Jouer
- **Écran titre** : Gauche/Droite pour choisir le stage, Start pour jouer, Select pour CONFIG (inchangé).
- **Émulateurs** : validé sous **Mesen 2.2.1**. SA-1 Root est annoncé compatible avec bsnes, Snes9x et le matériel réel (SD2SNES/FXPAK, cartouche SA-1). Ces derniers n'ont pas encore été testés avec Retro Rework.
- Le jeu requiert **32 Ko de BW-RAM** (en-tête SA-1 standard, géré par les émulateurs compatibles).
- **Non compatible** : versions européenne et japonaise, ZSNES.

---

## English

With **Retro Rework**, I revisit Super R-Type (Super Nintendo, Irem, 1991). I run this personal project with help from AI tools.

My patch **includes Vitor Vilela's SA-1 Root v1.3 acceleration**, which removes the original game's slowdown. I also add:
- **on-the-spot respawn**: after losing a life, your ship reappears where it was destroyed instead of going back to the checkpoint;
- **a main-menu Stage Select**: `< STAGE 1 >` to `< STAGE 7 >`, changed with Left/Right on the title screen.

See [CHANGELOG.md](CHANGELOG.md) for details.

> No ROM is provided. You must own an original Super R-Type cartridge and dump your own copy.

### Requirements
1. **Your original Super R-Type (USA) ROM**, unheadered (1,048,576 bytes):
   - SHA-256 `05c7f6461209020785fba33007e1830820aa44ada4b1a6f991d936bf2335b15b`
   - CRC32 `8B22C830`
2. **My single cumulative patch**: [Super-R-Type-Retro-Rework-v1.0.bps](patches/Super-R-Type-Retro-Rework-v1.0.bps) (open the file, then use the download button). SA-1 Root is already included; do not apply it separately.
3. **A BPS patching tool**, for example:
   - [Flips](https://sneslab.net/tools/floating.zip);
   - [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) (in your browser);
   - [beat](https://www.romhacking.net/utilities/893/).

### Installation (one step)
Apply `Super-R-Type-Retro-Rework-v1.0.bps` to your original Super R-Type (USA) ROM.

The result must have SHA-256 `0a5b3a784a0cceffeaf954812235341c8d3bb93b304158547ebb8347ab14257e` (CRC32 `36CBF8CA`).

BPS checks the input ROM. If your tool rejects the patch, the ROM is not the right one:
- European or Japanese version;
- 512-byte header (1,049,088-byte file);
- already modified ROM, for example already patched with SA-1 Root.

Checksums are also listed in [CHECKSUMS.sha256](CHECKSUMS.sha256).

### Playing
- **Title screen**: Left/Right to choose the stage, Start to play, Select for CONFIG (unchanged).
- **Emulators**: validated on **Mesen 2.2.1**. SA-1 Root is stated to work on bsnes, Snes9x and real hardware (SD2SNES/FXPAK, SA-1 cartridge); these have not been tested with Retro Rework yet.
- The game requires **32 KB of BW-RAM** (standard SA-1 header, handled by compatible emulators).
- **Not compatible**: European and Japanese versions, ZSNES.

---

Super R-Type © 1991 Irem. SA-1 Root © Vitor Vilela. I run Retro Rework as a non-commercial fan project, without affiliation with or endorsement by Irem, its successors or Nintendo. See [CREDITS.md](CREDITS.md).


[Rapport de validation / Validation report](docs/VALIDATION.md)
