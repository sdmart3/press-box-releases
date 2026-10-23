# Changelog

## 0.2.1 (draft)

- Final mod title and category: the picker mod is now "Press Box Picker" (Dynasty category), file `Press-Box-Picker-0.2.4.fbmod`.
  Same picker code as before. The plugin files are unchanged from 0.2.0 (tool version 0.2.0 inside).

## 0.2.0 (draft)

- In-game picker: choose one of the week's best 7 CPU-vs-CPU games from the hub item "Scouting", the side by picking the team
  from the list, and the mode from the hub item "Game Prep" (One = Play, Two = Coach, Three = Watch).
- `modes` now defaults on (`modes = 1`): the watch and coach parts are installed at start, unarmed. Nothing is switched on
  until the picker asks for it for one game.
- The old fixed away-side and home-side mods are gone, replaced by the picker mod.
- The tool is named Press Box.
- Known limits: best 7 games only until paging; mode labels read One / Two / Three; results count for the two computer teams
  only; not in the same load as Playoff Mode or Playoff Customizer; duplicate "EA SPORTS Network" hub entries are cosmetic.

## 0.1.0 (never released)

First draft: play, watch or coach one automatically picked CPU-vs-CPU game, settings in `anygame.ini`.
