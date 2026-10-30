# Press Box

**Play or watch any CPU-vs-CPU game in your dynasty, every week through the title game.**

Press Box is an add-on for College Football 27 dynasty mode. Pick any game between two computer teams on the Schedule, and
at the controller screen choose what you do: move to a team to play it, or leave the controller in the middle to watch.
It works the same way in your own games.

- **Works with the October 29 game update.**
- **New in 0.7.1:** *Take this game* works the first time, even before your first Advance. In a watched game press Start for the pause menu
  (Resume keeps watching; Super Sim and Quit work). Kicks never wait in a watched game on the October 29 update.
- **0.7.0, one flow for everything:** *Take this game* on the Schedule, then the controller screen decides. Move your
  controller to a team to **play** it. Leave it in the middle to **watch**. The old "Play as / Coach as / Watch this game"
  menu is gone.
- **Coaching** is the game's own Coach Mode + Autosnap (Settings), switched on for that game and off again for your normal games.

## How to use it

1. On the dynasty hub go to **EA SPORTS Network > Scores / Schedules**.
2. Highlight a game this week between two computer teams and press **A** (Actions). Pick **Take this game**. The game shows up
   as a card on your hub right away.
3. Open the card and start the game the same way you start your own. You land on the controller screen.
4. On the controller screen:
   - **Move your controller to a team and press Accept:** you play that team (home or away, your choice).
   - **Leave the controller in the middle and press Accept:** you **watch**. Both teams are played by the computer. Press Start any time
     for the game's pause menu (Resume keeps watching; Super Sim and Quit work as usual).

![A Press Box game card on the hub](screenshots/shot-card.png)

![Playing a CPU-vs-CPU game as the team you took](screenshots/shot-playing.png)

Good to know:

- **Release game** (in the same menu) drops the card. That game is simmed like any other.
- **As many games as you like**, up to 15 extra games a week.
- **Games you took but didn't play** are simmed as normal when you Advance.
- **The result counts for the two computer teams only.** Your record, XP and coach record don't change.
- **Your own game:** press A on it and you get the game's normal Force Win popup, nothing from Press Box. Use the controller
  screen instead (next section).
- **Playing signed out of EA:** the "Offline Warning" popup on the Dynasty Play button is gone. You don't need the No Offline
  Warning mod for it (see Known issues if you use that mod).

### Coaching a game

Press Box no longer has its own Coach Mode. Use the game's: in **Settings** turn on **Coach Mode** and **Autosnap**, take
the game and play it (the computer snaps the ball, you pick the plays). Turn both off again for your normal games.

### The playoffs

From the conference championship week through the title game the menu has one more entry: **Add every playoff game: ON**.
The entry appears after your first Take this game / Release game, or after an Advance. With it on, every College Football Playoff game between two computer teams gets a card as soon as each round is set, through
the title game, and you choose play or watch for each one at its controller screen like any other card. Pick **OFF** to stop.
Your own playoff games are never touched. You can still take any postseason game yourself with **Take this game**.

## Your own games: play either team, or watch

Before one of your own dynasty games the game shows the controller screen with your controller sitting on your team. In the
stock game it is locked there. With Press Box you can move it, the same way as in Play Now.

1. Start your game as usual. You land on the controller screen.
2. Push the left stick toward the other team's side to play them, or leave the controller in the middle to watch your own
   game.
3. Press **Accept**.

- **Leave the controller on your team** and you play your own team, exactly as before.
- **Away games:** the controller starts on your team (not the home team), so one habitual press of Accept still plays your
  own team.
- **Watching your own game:** the computer plays both teams and the result counts for your team as usual.
- **Your own custom playbook:** the game can only load it for your own team. When you move to the other team, Press Box uses
  that team's own book for it. If it can't find it, the controller goes back on your team and `anygame.log` says why.

What counts for whom when you play the opponent:

- **The result is real.** The final score, win or loss, standings and rankings go to the two real teams. If you play the
  opponent and win, your team loses.
- **Your record, coach XP and weekly goals follow your team,** which the computer plays. You can't complete your goals or
  earn your team's XP by playing the other side.
- **The opponent gets nothing that is only for the user.** Its coach and team progress as for any computer team.
- Player stats go to the players who played, on their own teams.

Not tested yet: resuming such a game from a mid-game save. **Avoid Super Sim > End Of Game when you are playing the opponent.**

This needs **both halves**: Press Box Picker 0.7.1 (the controller screen part) and the 0.7.1 plugin files (`anygame.dll`).
Don't mix 0.7.1 files with older ones. You can turn the side select off with `ctrl_select = 0` (see Settings).

## Tips

- **Watch: the computer stays in control.** For a watched game Press Box keeps both teams with the computer the whole way, even
  if a controller comes back from the pause menu, so a kickoff or punt doesn't wait for a play call nobody is going to make. If a
  watched game ever does wait 30 seconds or more in one place, Press Box writes a line about it in `anygame.log`.
- **Coach Mode kicks wait for your pick.** In the game's own Coach Mode, kickoffs, punts and safety kicks have a kick-play call
  screen with no play clock, so the game waits for you. Choose the kick and it carries on.

## What's in the download

```
README.md                            this file
CHANGELOG.md                         what changed
Press-Box-Picker-0.7.1.fbmod         the picker mod (import it in the Mod Manager)
Manual install\Plugins\              the files that go in your Mod Manager's Plugins folder
Compatibility patches\               one patch per mod that clashes with Press Box (see below), PATCHES.txt
```

## Requirements

- College Football 27 (PC) and the MMC Mod Manager. You launch the game from the Mod Manager.
- A dynasty.

## Install

1. Close the game and the Mod Manager.
2. Unzip the download anywhere.
3. Open the `Manual install\Plugins` folder from the download. Copy **everything in it** (`AnyGamePlugin.dll` and the
   `AnyGame` folder) into your Mod Manager's `Plugins` folder. That's the folder next to `MMCModManager.exe`. If there is
   no `Plugins` folder, create one.
4. Start the Mod Manager and import `Press-Box-Picker-0.7.1.fbmod` (Import, or drag it in). It shows up in the Dynasty
   category as "Press Box Picker". Turn it on.
5. **Restart the Mod Manager** if it was open while you copied the files. It only loads plugins when it starts.
6. Launch the game from the Mod Manager as usual.

**Updating from 0.7.0 or earlier:** replace the picker (turn off and remove the old Press Box Picker, import
`Press-Box-Picker-0.7.1.fbmod`) **and** copy the new `anygame.dll` over the old one. Keep your `anygame.ini`: the new settings
are missing from an old file and then simply use their defaults (on). Both halves are needed. Cards made with an older Press Box menu still play the way they were picked.

You end up with:

```
<Mod Manager>\Plugins\AnyGamePlugin.dll
<Mod Manager>\Plugins\AnyGame\   anygame.dll, anygame.ini (your settings), plugin.cfg, logs
```

## Compatibility patches

Some dynasty mods change the same game files as Press Box, so on their own one of the two stops working. The
`Compatibility patches` folder in the download has one small patch for each of them. **Needs the Press Box plugin and Press
Box Picker installed first** (the Install steps above), then:

| You use | Patch file |
|---|---|
| Playoff Customizer 1.3.0 | `Press-Box-x-Playoff-Customizer-1.3.0-patch.fbmod` |
| Dynasty Customizer 1.1.0 | `Press-Box-x-Dynasty-Customizer-1.1.0-patch.fbmod` |
| Conference Customizer 1.0.2 | `Press-Box-x-Conference-Customizer-1.0.2-patch.fbmod` |
| AIO Dynasty Mod v1.3.1 | `Press-Box-x-AIO-Dynasty-1.3.1-patch.fbmod` |

**Load order in the Mod Manager (top to bottom):**

1. The other mod (for example Playoff Customizer 1.3.0)
2. Press Box Picker 0.7.1
3. The matching patch, **last** (the bottom of the list)

Import the patch like the picker and keep all three on. `PATCHES.txt` in that folder says the same in short.

Good to know:

- **Built for the October 29 game update:** these patches are made for the October 29 versions of those mods (Playoff
  Customizer 1.3.0, Dynasty Customizer 1.1.0, Conference Customizer 1.0.2, AIO Dynasty Mod v1.3.1). Older versions of those mods
  are not covered; update the mod first.
- **Use the patch for your exact version.** Each patch is made for one version of the other mod and says so in its
  description. If that mod updates, wait for a new patch.
- **Playoff Customizer, Dynasty Customizer and AIO:** the **Add every playoff game** entry isn't in the patched menu. You can
  still take any playoff game yourself from the menu (Take this game), and Release game drops it. The Playoff Customizer
  patches work in a dynasty you already have running with that version.
- **Dynasty Customizer, Conference Customizer and AIO** are for new dynasties: start the dynasty with the mod and its patch on.
- **Conference Customizer:** everything in Press Box works as usual, including Add every playoff game.
- If a patch is missing or out of order, either the Press Box menu disappears (safe: the other mod works normally) or the
  other mod's own changes are lost. If you see either, check the order above.

Playoff Customizer, Dynasty Customizer, Conference Customizer and AIO Dynasty Mod are by their authors; the patches contain
their files with permission.

## Settings

Settings are in `<Mod Manager>\Plugins\AnyGame\anygame.ini`. Open it in Notepad (`1` = on, `0` = off), save it, and
start the game. **The file is read once when the game starts, so change it with the game closed.**

| Setting | Default | What it does |
|---------|---------|--------------|
| `play` | 1 | Makes the games you take play properly: your coach, the right playbook, the right home or away side. Needed for everything else. |
| `modes` | 1 | Cards made with an older Press Box menu ("Coach as" / "Watch this game") still play the way they were picked. Leave it at 1. |
| `watch` | 1 | Leave the controller in the middle of the controller screen and the game is watched, in a game you took and in your own game. 0 = a controller left in the middle is put back on a team. |
| `coach` | 0 | Leave at 0. To coach, use the game's own Coach Mode + Autosnap in Settings. |
| `watch_guard` | 1 | In a game you **watch**, both teams stay with the computer for the whole game, even if a controller comes back (for example from the pause menu). Only the watched game. |
| `watch_pause` | 1 | While you **watch**, press Start (or the menu button) and the game's own pause menu opens: Resume keeps watching, Super Sim and Quit work as usual. 0 = Start does nothing while you watch. |
| `stall_log` | 1 | Writes a line to `anygame.log` when a watched game waits in one place for 30 seconds or more. Troubleshooting only; changes nothing. |
| `ctrl_select` | 1 | Choose a team (or watch) on the controller screen, in a game you took and in your own games (see above). 0 = the game's own controller screen, where your controller stays on your team. |
| `exit_log` | 0 | 1 = write a line to the log whenever the game closes itself. Only for troubleshooting. |

Your settings are never overwritten by copying a newer version over the old one (copy everything except
`anygame.ini` and `plugin.cfg`, or keep a backup).

## Known issues

- **Playing the opponent in your own game** works: the result counts for the real teams, so beating your own team costs
  your team the win, coach XP and goals. Not tested yet: resuming from a
  mid-game save. **Avoid Super Sim > End Of Game in a game where you are playing the opponent.**
- **Mods that unlock the controller screen or change `common/ui/node_fe/scriptpod.ast`** clash with the controller select
  part of the picker. Use one of them, not both.
- **Mods that change the dynasty hub screens or expression files.** Playoff Customizer (1.3.0), Dynasty
  Customizer, Conference Customizer and AIO Dynasty Mod work through their patch (see Compatibility patches). Others, such as
  Playoff Mode or DRI+, still clash with Press Box: use one of them, not both. Without the patch, in a dynasty that already
  holds Playoff Customizer data the Press Box menu does nothing.
- **No Offline Warning mod:** Press Box now removes the same Dynasty Play popup itself, so you can turn that mod off. If you keep
  it (for its sign-in popup at start-up), put it **above** Press Box Picker in the Mod Manager list, or the Press Box menu goes
  missing.
- **An extra "Practice" item on the hub** comes from Playoff Customizer, not from Press Box.
- Never use **Super Sim > End Of Game** on a Press Box card. The game can close itself.
- The card after a game can show the score from the other team's side. It is cosmetic.
- **Watch mode:** Press Box now keeps the computer in control of both teams for the whole watched game (`watch_guard`), so a
  controller that comes back from the pause menu doesn't hold up a kickoff or punt. If a watched game still waits somewhere,
  Press Box logs it (`stall_log`): send `anygame.log` and `anygame-status.json`.
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

- **No Press Box menu, only the normal popup:** check the mod is on in the Mod Manager. The menu shows on this week's
  unplayed games between two computer teams; your own game always shows the normal popup.
- **"access denied" in plugin.log:** the game runs as administrator. Run the Mod Manager as administrator too.
- **`failed` after a game update:** the game changed something. Look for a Press Box update. Your games stay normal.
- **The controller still can't leave your team in your own game:** check `ctrl_select` is 1 in `anygame.ini`, that Press Box
  Picker **0.7.1** is on, and that the new `anygame.dll` is the one in the `AnyGame` folder. After a game update the status
  can read "partial": the controller select turns itself off and the rest keeps working.
- **`NOTE: play = 0` in `anygame.log`:** `play` is off in your `anygame.ini`, so Press Box does nothing in the games you take.
  Set it back to 1.

When reporting a problem, send the three files above.

## Uninstall

Close the game and the Mod Manager. Delete `<Mod Manager>\Plugins\AnyGamePlugin.dll` and the
`<Mod Manager>\Plugins\AnyGame` folder, and turn off or remove the mod in the Mod Manager.
