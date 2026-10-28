# Changelog

## 0.6.3

- **A menu on every CPU-vs-CPU game.** In EA SPORTS Network > Scores / Schedules, press A on any game this week between two
  computer teams: Play as either team, Coach as either team, Watch this game, or Release game. No more picking from a list of
  the week's best games.
- **Cards on the hub.** Every game you take shows up as a card on your hub right away. Pick another entry on the same game and
  it stays one card, switched to the new side or mode. Release game drops the card.
- **As many games as you like**, up to 15 extra games a week.
- **The playoffs.** From the conference championship week through the title game the menu also has "Watch every playoff game":
  turn it on and every College Football Playoff game between two computer teams gets a Watch card as each round is set. You can
  also Play, Coach or Watch any championship game, bowl or playoff game yourself from the menu.
- **Games you took but didn't play are simmed as normal** when you Advance. Results count for the two computer teams only; your
  record, XP and coach record don't change.
- **Your own game is untouched.** Pressing A on it gives the game's normal Force Win popup, in every week and on every screen.
- **Scouting and Game Prep are gone.** The old hub items are retired, and the first Advance with this version clears them and any
  old picks from saves made with an older Press Box.
- Picker mod: `Press-Box-Picker-0.6.3.fbmod` (replaces `Press-Box-Picker-0.2.4.fbmod`). The plugin files are unchanged from 0.2.1.
- Known issues: Coach mode can sit for 2 to 5 minutes on a punt call before the computer snaps (it isn't frozen, wait); other
  mods that change the dynasty hub screens or expression files (Playoff Customizer, Dynasty Customizer, Playoff Mode, DRI+ ...)
  clash, so use one (a Playoff Customizer compat patch is in testing); never use Super Sim > End Of Game on a Press Box card.

## 0.3.0 to 0.6.2 (test builds, never released)

## 0.2.1

- Final mod title and category: the picker mod is now "Press Box Picker" (Dynasty category), file `Press-Box-Picker-0.2.4.fbmod`.
  Same picker code as before. The plugin files are unchanged from 0.2.0 (tool version 0.2.0 inside).
- Known limit: the picker works in regular-season weeks only; the championship, bowl and playoff weeks offer no Scouting / Game Prep items.
- Known limit: not with Playoff Customizer, Dynasty Customizer or Playoff Mode in the same load; Conference Customizer needs a compat build.

## 0.2.0

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
