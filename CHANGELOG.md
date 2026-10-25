# Changelog — Super R-Type Retro Rework

## v1.0

Base: Super R-Type (USA) + SA-1 Root v1.3 (Vitor Vilela). All SA-1 Root code is kept unchanged.

### Ajouts / Additions
- **Respawn sur place / On-the-spot respawn**
  - FR :
    - Tant qu'il reste des vies, le vaisseau réapparaît à l'endroit de sa destruction au lieu de revenir au point de contrôle.
    - Le jeu cherche une position libre de décor à proximité.
    - La musique continue, avec un son de mort et de réapparition dédié.
    - L'armement revient à l'équipement de base, comme après une mort normale.
    - Pendant la rentrée, le vaisseau est intangible et ne peut pas tirer. La protection se termine dès que la zone est dégagée ; le joueur peut se déplacer pour la quitter.
    - Sans vie restante, le game over et le Continue d'origine s'appliquent.
  - EN :
    - While lives remain, the ship reappears where it was destroyed instead of returning to the checkpoint.
    - The game looks for a nearby position free of scenery.
    - Music keeps playing, with dedicated death and respawn sounds.
    - Weapons return to the base loadout, as after a normal death.
    - During re-entry the ship is intangible and cannot fire. Protection ends as soon as the area is clear; the player can move to leave it.
    - With no lives left, the original game over and Continue apply.
- **Stage Select au menu principal / Main-menu Stage Select**
  - FR :
    - Ligne `< STAGE n >` (stages 1 à 7) au-dessus de PUSH START.
    - Gauche/Droite pour changer de stage, avec bouclage de 7 à 1, et le son du curseur d'origine.
    - Start lance la partie au stage choisi, avec les conditions standard : 3 vies, équipement de base, difficulté choisie dans CONFIG.
    - Le choix est conservé jusqu'à l'extinction ou au reset.
    - Il n'y a pas de nouveaux graphismes : les chevrons et les lettres viennent de la police d'origine.
  - EN :
    - `< STAGE n >` line (stages 1 to 7) above PUSH START.
    - Left/Right to change stage, wrapping from 7 to 1, with the original cursor sound.
    - Start begins the game at the chosen stage with standard conditions: 3 lives, base loadout, difficulty from CONFIG.
    - The choice is kept until power-off or reset.
    - There are no new graphics: chevrons and letters come from the original font.

### Inchangé / Unchanged
- FR : accélération SA-1 Root ; CONFIG (LEVEL, SOUND, BGM, S.E) ; démo ; Continue ; codes et Stage Select cachés d'origine ; graphismes et sons d'origine.
- EN: SA-1 Root acceleration; CONFIG (LEVEL, SOUND, BGM, S.E); attract demo; Continue; original hidden codes and pause-menu stage select; original graphics and sound.

### Comportements connus / Known behaviour
- FR :
  - Commencer à un stage avancé ne marque pas les stages précédents comme terminés, comme avec le Stage Select caché d'origine. La séquence de fin peut donc différer de celle d'une partie complète.
  - Si le joueur pousse le vaisseau contre le sol ou le plafond à la fin d'une rentrée, la protection dure tant qu'il reste collé au décor. S'en éloigner y met fin.
- EN:
  - Starting at a later stage does not mark earlier stages as cleared, as with the original hidden stage select. The ending sequence may therefore differ from a full playthrough.
  - If the player pushes the ship against the floor or ceiling at the end of a re-entry, protection lasts while it stays against the scenery. Moving away ends it.
