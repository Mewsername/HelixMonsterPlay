# Helix Monster Play

Ever wanted to be the monster for once? This is a mod for **Helix: Feed The World** where you play the monster and Helix has to deal with you for a change. 18+ only, and still very WIP.

Full intro with screenshots: https://mewsername.github.io/HelixMonsterPlay/

![Playing as Ezmir](https://mewsername.github.io/HelixMonsterPlay/shots/ezmir.jpg)

## What it does

- **Play as the monster:** you vs an AI Helix that circles you, dodges, learns your attacks, and gets scared or friendly depending on how you treat it.
- **Play online:** grab a friend. One of you is Helix, the other is the monster, each on your own PC. There's a lobby, chat, and you can join through Steam or with a short code.

Works with Wolfo, Ezmir, Yama, Gridiron, Meilu and Sholstim.

## Install

1. [Download the mod](https://github.com/Mewsername/HelixMonsterPlay/releases/latest/download/HelixMonsterPlay.zip).
2. Run the game once. It already comes with BepInEx, so you don't need anything else.
3. Unzip it into your game folder (the one with `HelixFTW.exe`).
4. Start the game and click past the 18+ notice and the title screen. You'll see **Mode** and **Play online** in the main menu.

Want it gone? Just delete `BepInEx\plugins\HelixMonsterPlay`.

## Controls

| Key | What it does |
|---|---|
| WASD / left stick | Move |
| Mouse / right stick | Camera |
| Shift / hold B | Sprint |
| Left click / RB | Attack |
| Right click / RT | Grab |
| Shift + click | Sprint attacks |
| R / Y | Special move |
| Space | Dodge (if your monster has one) |
| Tab | Full move list, then 1-9 and 0 to use any move from it |
| F6 | Switch mode (monster, just watching, normal Helix) |
| F7 | Change Helix's personality |
| F8 | Hide the HUD |

**Helix in your belly:** hold left click to fill the belly action arrow, right click for the wait arrow. R spits Helix back out.

**Carrying Helix:** some monsters carry Helix somewhere, like Yama taking it to her den. You do the walking. A purple light marks the spot, just stand on it.

## Playing online

1. You both need the same version of the mod. Hit **Play online** in the main menu.
2. Pick how to connect:
   - **Steam** (easiest, you both need Steam open): the host picks **Host** and who they want to play, then invites their friend from the lobby. The friend goes to **Steam > Join**, or just accepts the invite.
   - **Join code** (no Steam): the host picks **Host** and the mod opens the port on their router by itself. The lobby shows a code with a **Copy** button. The friend goes to **Join code > Join** and pastes it.
3. In the lobby you can chat, the host picks the stage and can swap roles. The friend hits **Ready**, the host hits **Start**.
4. During the fight, Enter opens the chat. When the host goes back to the menu, you both end up in the lobby again.

Good to know:

- Steam will say you're playing "Spacewar" while you use the Steam option. That's normal, the mod borrows Valve's free test app to make invites work. You can turn Steam off with `UseSteam = false` in the config.
- Code not working? Some routers don't allow opening ports automatically, and some internet providers share one address between lots of people. The lobby tells you if that happens. Use Steam instead, or a Tailscale / ZeroTier / Hamachi network. Windows might also ask to let the game through the firewall the first time you host, just allow it.
- It's one friend at a time, and the connection isn't encrypted, so only play with people you know.
- If the connection drops, the friend goes back to the menu and the AI takes over the other character again.
- Lock-on doesn't work for a friend playing Helix.

## Settings

The config file `BepInEx\config\com.monsterplay.helixftw.cfg` shows up after the first start:

- `StartMode`: what mode you start in (MonsterPlay, Spectate or Vanilla)
- `Personality`: Helix's personality (Brave, Friendly, Timid, Submissive or Mixed)
- `DodgeSkill`: how good Helix is at reading and dodging your attacks, 0 to 1
- `AttackRate`: how eager Helix is to go in
- `ShowThoughts`: show what Helix is thinking on the HUD
- `WalkSpeedMultiplier`: makes the monster walk faster than its slow stalk
- `CameraDistanceMultiplier`: how far the camera sits from the monster
- `SwapVictoryText`: Victory / Game Over from the monster's point of view
- `Online`: your name, the port, and whether to use Steam

## Known issues

- A few moves only work in the situation they were made for, so things like counter attacks aren't in the move list.
- Lock-on is off while you play a monster.
- Ezmir's burrow digs toward Helix by itself and comes back up within about 10 seconds.
- There will be bugs, especially online. If something breaks, open an issue or send me `BepInEx\LogOutput.log` and tell me what you were doing when it happened.

## Credits

Helix: Feed The World is made by Serkular, Alsnapz and Crebalt. No game files are included here, and please don't sell or reupload the game.

Uses BepInEx and HarmonyX. The Steam stuff uses [Steamworks.NET](https://github.com/rlabrecque/Steamworks.NET) (MIT, license included) and Valve's steam_api64.dll.
