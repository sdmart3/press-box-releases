# Changelog

## 0.7.1

- **Take this game works the first time, even before your first Advance.** 0.7.0 needed one week Advance first.
- **Watching a game: press Start for the pause menu.** Resume keeps watching; Super Sim and Quit work.
- **Kicks never wait in a watched game on the October 29 update.** The watch guard didn't turn on in 0.7.0; it does now.
- **Add every playoff game** appears after your first Take / Release or an Advance.
- Files: `Press-Box-Picker-0.7.1.fbmod` (replaces 0.7.0), a new `anygame.dll` (tool 0.3.0, updated build: its log still reads 0.3.0) and the four Compatibility patches rebuilt for
  the new picker. The loader `AnyGamePlugin.dll` is unchanged. Use the picker and `anygame.dll` together.
- New setting `watch_pause` (default 1). Copy over your old `anygame.ini` and it uses the default.

## 0.7.0

- **One flow for every game: take it, then the controller decides.** On the Schedule pick **Take this game** (the old "Play as /
  Coach as / Watch this game" entries are gone). At the controller screen move your controller to a team and press Accept to
  play that team, home or away. Leave the controller in the middle and press Accept to watch: both teams are played by the
  computer. A game you took no longer forces you onto the team you picked.
- **Move to the other team to play that team.** The game now loads the team your controller left like any other team. (Tool 0.3.0, build
  248186ef: earlier test builds could stop the game at its start after a controller visit.) If you have a custom playbook of your own, the game can only load it for your own team: Press Box looks up the
  other team's own book and uses it, and if it can't find it the controller goes back on your team and `anygame.log` says why.
- **Watch your own game too.** In your own dynasty game, leave the controller in the middle to let the computer play both
  teams. The result counts for your team as usual. Move the controller to the other team to play them.
- **Safe watching.** The game can't start with no controller on a team, so Press Box puts the controller on a team, lets the game load, then takes every controller off.
- **Coaching is the game's own Coach Mode.** Press Box no longer has its own Coach Mode. In Settings turn on Coach Mode and
  Autosnap for the game you take, and turn them off again for your normal games. Cards made with a 0.6.x menu still play the
  way they were picked.
- **Add every playoff game: ON** (replaces "Watch every playoff game") makes a card for every computer-vs-computer playoff game; you choose play or
  watch for each at its controller screen.
- **Works with the October 29 game update.** The picker, `anygame.dll` (tool version 0.3.0) and the four Compatibility patches are
  built for the new game version.
- **Compatibility patches** for the October 29 versions of Playoff Customizer 1.3.0, Dynasty Customizer 1.1.0, Conference
  Customizer 1.0.2 and AIO Dynasty Mod v1.3.1. The patches for the older versions of those mods are gone: update the other mod first.
- Settings: `watch` is now on by default (it means "controller in the middle = watch"); `coach` stays 0 and is not needed.
- Files: `Press-Box-Picker-0.7.0.fbmod` (replaces 0.6.5) and a new `anygame.dll`. The loader `AnyGamePlugin.dll` is unchanged. Use
  both new files together.
- Known issues: avoid Super Sim > End Of Game in a game where you are playing the opponent. Not tested yet: resuming such a game from a mid-game save.

## 0.6.5

- **Play either team in your own games.** At the controller screen before your own dynasty game, move the stick to the other
  team like in Play Now and press Accept: you play the team your controller is on. Leave it in the middle and you play your own
  team. In an away game the controller starts on your team. On a game you took with Press Box it stays on the team you picked.
  The result is real: if you play the opponent and win, your team loses; your record, coach XP and weekly goals follow your
  team. New setting `ctrl_select` (1 = on). Needs the new picker **and** the new `anygame.dll`.
- **Watch keeps the computer in control.** In a watched game both teams stay with the computer for the whole game, even if a
  controller comes back from the pause menu, so a kickoff or punt doesn't wait for a play call nobody makes. New setting
  `watch_guard` (1 = on).
- **Long waits are logged.** If a watched or coached game waits 30 seconds or more in one place, a line goes in `anygame.log`.
  New setting `stall_log` (1 = on). It changes nothing in the game.
- **Coach mode: the old "punt wait" is a tip, not a bug.** Kickoffs, punts and safety kicks have a call screen with no play
  clock, so the game waits for your pick. Choose the kick and it carries on.
- `anygame.log` says `NOTE: play = 0` when `play` is switched off in `anygame.ini`. The `watch` and `coach` notes in the ini are
  reworded.
- **Works with the October 29 game update.** The picker, `anygame.dll` and all six Compatibility patches are rebuilt for the new game version.
- The Compatibility patches for Playoff Customizer, Dynasty Customizer, Conference Customizer and AIO Dynasty Mod carry their authors' files, which were made for the old game. The Mod Manager refuses them until those mods are updated for the new game by their authors. Press Box on its own is not affected.
- Files: `Press-Box-Picker-0.6.5.fbmod` (replaces 0.6.4) and a new `anygame.dll` (tool version 0.2.2). The loader `AnyGamePlugin.dll`
  is unchanged.
- Known issues: avoid Super Sim > End Of Game in a game where you are playing the opponent until it has been tested. Not tested yet:
  the opponent's playbook and play-call screen, and resuming such a game from a mid-game save.

## 0.6.4

- **Taking a game works with a crowded request list.** With some dynasty mods on (Playoff Customizer keeps many open requests),
  picking an entry in the menu could do nothing. The menu now finds its request either way.
- **No "Offline Warning" popup when you play signed out.** The popup on the Dynasty Play button is gone, so you don't need the No
  Offline Warning mod for it.
- **Compatibility patches included.** The new `Compatibility patches` folder has a patch for Playoff Customizer 1.1.0, 1.2.0 and
  1.2.1, Dynasty Customizer 1.0.0, Conference Customizer 1.0.0 and AIO Dynasty Mod v1.3. Load the other mod, then Press Box
  Picker, then its patch last. See the README and `PATCHES.txt`.
- The extra "Practice" item some players see on the hub comes from Playoff Customizer, not from Press Box.
- `anygame.ini`: clearer notes on `watch` and `coach`. They aren't needed to watch or coach a game (pick it in the menu); 1 forces
  every taken game into that mode.
- Picker mod: `Press-Box-Picker-0.6.4.fbmod` (replaces `Press-Box-Picker-0.6.3.fbmod`). The plugin files are unchanged.

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
