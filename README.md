# Press Box

**Step into any of the week's best CPU-vs-CPU games.**

Press Box is an add-on for College Football 27 dynasty mode. Each week you pick one of the week's best 7 games between two
computer teams, choose which side to take, and choose how to take part in it. Your own team's game is never touched.

- **Play**: take the controller for one side and play the game yourself.
- **Coach**: the game's Coach Mode for that game only. You pick the plays, the computer snaps the ball.
- **Watch**: both teams are played by the computer and you watch.

## How to use it

Everything is picked from two items on the hub:

1. **Scouting**: pick the game (one of the week's best 7 CPU-vs-CPU games). The side you take is the team you choose from
   the list.
2. **Game Prep**: pick the mode. The labels read **One**, **Two** and **Three**:
   - One = Play
   - Two = Coach
   - Three = Watch

Then play the week as usual. The picked game shows up as the game card for that week. The link is cleared when you advance
the week.

## What's in the download

```
README.md                            this file
CHANGELOG.md                         what changed
Press-Box-Picker-0.2.4.fbmod         the picker mod (import it in the Mod Manager)
Manual install\Plugins\              the files that go in your Mod Manager's Plugins folder
```

## Requirements

- College Football 27 (PC) and the MMC Mod Manager. You launch the game from the Mod Manager.
- A dynasty, in a regular-season week.

## Install

1. Close the game and the Mod Manager.
2. Unzip the download anywhere.
3. Open the `Manual install\Plugins` folder from the download. Copy **everything in it** (`AnyGamePlugin.dll` and the
   `AnyGame` folder) into your Mod Manager's `Plugins` folder. That's the folder next to `MMCModManager.exe`. If there is
   no `Plugins` folder, create one.
4. Start the Mod Manager and import `Press-Box-Picker-0.2.4.fbmod` (Import, or drag it in). It shows up in the Dynasty
   category. Turn it on.
5. **Restart the Mod Manager** if it was open while you copied the files. It only loads plugins when it starts.
6. Launch the game from the Mod Manager as usual.

You end up with:

```
<Mod Manager>\Plugins\AnyGamePlugin.dll
<Mod Manager>\Plugins\AnyGame\   anygame.dll, anygame.ini (your settings), plugin.cfg, logs
```

## Settings

Settings are in `<Mod Manager>\Plugins\AnyGame\anygame.ini`. Open it in Notepad (`1` = on, `0` = off), save it, and
start the game. **The file is read once when the game starts, so change it with the game closed.**

| Setting | Default | What it does |
|---------|---------|--------------|
| `play` | 1 | Makes the picked game play properly: your coach, the right playbook, the right home or away side, and the hub card shows the result from the side you played. Needed for everything else. |
| `modes` | 1 | Lets the picker choose Play, Coach or Watch for the picked game. Leave it at 1 to use the picker. With 0 the picker's Coach and Watch choices do nothing. |
| `watch` | 0 | 1 = every picked game is watched computer vs computer, whatever the picker says. Normally leave at 0. |
| `coach` | 0 | 1 = every picked game is played in Coach Mode, whatever the picker says. Normally leave at 0. |
| `exit_log` | 0 | 1 = write a line to the log whenever the game closes itself. Only for troubleshooting. |

Turn on only one of `watch` and `coach` at a time.

Your settings are never overwritten by copying a newer version over the old one (copy everything except
`anygame.ini` and `plugin.cfg`, or keep a backup).

## Known limits

- Only the week's best 7 games are offered for now, until the list can page.
- The mode labels read One, Two and Three (see above).
- The result counts for the two computer teams only. Your own record and XP are untouched.
- **Not with Playoff Customizer or Playoff Mode in the same load.** They change the same game logic. Don't use them
  together.
- **Watch mode:** a controller can rejoin a team from the pause menu. Back out of it and the computer keeps playing.
- You may see extra duplicate "EA SPORTS Network" entries on the hub. They are cosmetic.
- Don't resume a quit Press Box game from a mid-game save.
- Press Box stays out of the way if another tool in your game already runs its own copy of this feature.

## Troubleshooting

Everything is in `<Mod Manager>\Plugins\AnyGame\`:

- `plugin.log`: whether the plugin loaded the DLL into the game. If it is missing or empty, the Mod Manager was open
  when you installed. Restart it and launch from it.
- `anygame.log`: what Press Box did in the game.
- `anygame-status.json`: the current state (`installed`, `idle`, `standing_aside` or `failed`, with the reason). Open it in
  Notepad.

Common cases:

- **No Scouting or Game Prep items:** check the mod is on in the Mod Manager and you are in a regular-season week.
- **"access denied" in plugin.log:** the game runs as administrator. Run the Mod Manager as administrator too.
- **`failed` after a game update:** the game changed something. Look for a Press Box update. Your games stay normal.

When reporting a problem, send the three files above.

## Uninstall

Close the game and the Mod Manager. Delete `<Mod Manager>\Plugins\AnyGamePlugin.dll` and the
`<Mod Manager>\Plugins\AnyGame` folder, and turn off or remove the mod in the Mod Manager.
