A guide on how to **download** and **install mods** for [PUBG: BATTLEGROUNDS](https://store.steampowered.com/app/578080/PUBG_BATTLEGROUNDS/) on PC.

PUBG modding is not what most people expect when they hear the word. There is no mod loader, no `.dll` files and no way to alter the base game. PUBG runs BattlEye, and touching the client is a ban, full stop.

What PUBG actually has is a **UGC system**: an official in-game editor that creators use to build custom game modes and maps, published as `.pugc` files on [CurseForge](https://www.curseforge.com/pubg-battlegrounds) and played through custom matches. Those are the "mods" this guide covers.

We use two of them as examples: [GIANTS TOYS](https://www.curseforge.com/pubg-battlegrounds/game-mods/giants-toys), where everything except you is enormous, and [Hide-and-Seek](https://www.curseforge.com/pubg-battlegrounds/game-mods/hide-and-seek), a party mode split into hiders and seekers.

[**View Guide On TMC (Recommended Due To Better Formatting)**](https://moddingcommunity.com/blog/how-to-install-mods-in-pubg/)

## Table Of Contents
* [Read This First](#read-this-first)
* [Requirements](#requirements)
* [What PUBG Mods Actually Are](#what-pubg-mods-actually-are)
* [Installing A Mod](#installing-a-mod)
    * [Downloading From CurseForge](#downloading-from-curseforge)
    * [Putting The File In The Right Place](#putting-the-file-in-the-right-place)
    * [Loading It In-Game](#loading-it-in-game)
* [The TMC App](#the-tmc-app)
* [Playing With Other People](#playing-with-other-people)
* [Consoles And Mobile](#consoles-and-mobile)
* [Managing Your UGC Files](#managing-your-ugc-files)
* [Making Your Own](#making-your-own)
* [Troubleshooting](#troubleshooting)
* [Conclusion](#conclusion)
* [See Also](#see-also)

## Read This First
**Do not install anything that claims to mod the PUBG client.** PUBG is a competitive online shooter protected by BattlEye. Injectors, DLL mods, config hacks and anything else that modifies the running game are cheats as far as the anti-cheat is concerned, and the result is a permanent hardware ban on your account.

Everything in this guide is content that PUBG Studios built the system for and that CurseForge hosts with their blessing. It is entirely safe, and it is the only kind of PUBG modding there is.

## Requirements
* A PC running **Windows 10** or later. PUBG also runs on Linux through Proton, though the UGC workflow below assumes Windows paths.
* **PUBG: BATTLEGROUNDS** on Steam. The game is free to play.
* A small amount of free space. `.pugc` files are usually a few MB at most.
* Friends, ideally. Most of the interesting UGC modes need more than one player.

## What PUBG Mods Actually Are
A PUBG mod is a single `.pugc` file. It describes a custom game mode or map built with PUBG's own in-game editor: the layout, the rules, the teams, the win conditions, the loot.

Because it is data for the editor rather than code, a `.pugc` file cannot do anything the editor cannot. It cannot change your character, give you an advantage in ranked, or alter the normal game in any way. It is closer in spirit to a Counter-Strike community map than to a Skyrim mod.

On CurseForge they are organised by the kind of experience they create, with categories like **Battle (Team)**, **Battle (Free-For-All)**, **Parkour** and **Casual**. Browsing those is a better way to find something worth playing than searching by name.

**NOTE** - PUBG Studios and CurseForge have run official UGC contests with substantial prize pools, most recently one with $95,000 across 46 creators. The quality at the top end is considerably higher than you might expect.

## Installing A Mod
### Downloading From CurseForge
1. Go to [CurseForge's PUBG section](https://www.curseforge.com/pubg-battlegrounds).
2. Find a mod. For this guide, open [GIANTS TOYS](https://www.curseforge.com/pubg-battlegrounds/game-mods/giants-toys).
3. Click **Download**.

You will get a single `.pugc` file, for example `GIANTS TOYSS 1.2.pugc`.

The CurseForge app does not manage PUBG UGC files for you the way it does Minecraft mods, so this is a plain browser download.

### Putting The File In The Right Place
PUBG reads UGC files out of a folder in your local app data, not out of the game install.

1. Press **Windows + R** to open the Run dialog.
2. Type `%localappdata%` and press Enter.
3. Navigate to `TslGame`, then `Saved`, then `UGC`.

The full path is:

```
C:\Users\<your username>\AppData\Local\TslGame\Saved\UGC
```

4. Copy the `.pugc` file into that folder.

If the `UGC` folder does not exist, create it. It is only made once the game has reason to use it.

**TIP** - You can paste `%localappdata%\TslGame\Saved\UGC` straight into the File Explorer address bar to jump there in one go. Right-click the folder and pin it to Quick access if you plan to collect a few of these.

### Loading It In-Game
1. Launch PUBG.
2. From the main menu, go to **Custom** and choose **UGC Alpha Map**.
3. Create a room.
4. Press **F10** to open the file loader.
5. Pick your `.pugc` file.
6. Press **P**, then **Play**.

The mode loads and you are in. Repeat the same steps for Hide-and-Seek or anything else you have downloaded, since each `.pugc` is loaded per room rather than installed permanently.

**NOTE** - The exact wording of these menus has shifted as the UGC system has developed, and individual mods sometimes have their own quirks. The mod's CurseForge description is worth reading, because creators normally note anything unusual about loading theirs.

## The TMC App
Mentioned for completeness rather than because PUBG needs it. [The TMC App](https://moddingcommunity.com/tmc-app) is our own mod manager and server browser, and since PUBG UGC is a single file dropped into a single folder, there is not a great deal for a mod manager to do here.

**PUBG is not in its supported games list**, and unless the UGC system grows considerably it is unlikely to be a priority. We are not going to pretend otherwise to get you to install something.

Where the app might earn its place for you is elsewhere: sandboxed mod profiles for the other games you play, a server browser with live latency graphs, and RCON. **It is in very early development** though, and its own README describes it as partially tested, so go in with that expectation.

It is **open source** under GPL-3.0 at [github.com/modcommunity/tmc-app](https://github.com/modcommunity/tmc-app). If you try it, [the issue tracker](https://github.com/modcommunity/tmc-app/issues) is where bug reports and feature requests are most useful, and pull requests are very welcome. Feedback at this stage shapes what the app becomes.

Installing it:

* **Linux**: one line, no root and no package manager.

```bash
curl -fsSL https://raw.githubusercontent.com/modcommunity/tmc-app/main/scripts/install.sh | sh
```

* **Windows**: the `setup.exe` or `setup.msi` from the [releases page](https://github.com/modcommunity/tmc-app/releases). There is a portable build too, though it does not register the launcher entry or the `tmc://` link handler.
* **macOS**: the `.dmg` from the same releases page.

## Playing With Other People
UGC modes run in custom matches, so the flow is the same as any other custom game:

1. The host loads the `.pugc` as described above and creates the room.
2. Other players join the custom match through the room's code or the custom match browser.

Only the host needs the file. Everybody else connects to the host's room and plays whatever is loaded there, which is a nice side effect of this being a server-authoritative system rather than a client mod.

Most UGC modes have a minimum player count to be worth anything. Hide-and-Seek in particular needs a group, since it divides everyone into two teams.

## Consoles And Mobile
PUBG is also on PlayStation, Xbox and mobile, and UGC is a PC feature. There is no way to load `.pugc` files on a console or a phone.

Crossplay is worth a quick word while we are here, because it is frequently misunderstood. PUBG console crossplay pairs **PlayStation and Xbox players together**, and PC players are in their own pool. PC and console players do not match with each other in normal play, and PUBG Mobile is a separate game entirely with its own accounts and progression.

So if you want to play UGC modes, everyone involved needs to be on PC.

## Managing Your UGC Files
There is no mod manager for this. The `UGC` folder is just a folder, and managing your collection means managing files.

* **Remove a mode**: delete its `.pugc` file.
* **Update a mode**: download the new version from CurseForge and replace the old file. Creators normally bump the version in the filename, so keeping the old one around does no harm beyond clutter.
* **Organise**: keeping them flat in `UGC` is what the game expects. Subfolders are not reliably picked up.

Because the files are small, backing up your collection is as simple as copying the folder somewhere.

## Making Your Own
If any of this appeals, the editor is built into PUBG and available to everyone. CurseForge and PUBG Studios publish a **How to Create Custom Modes** walkthrough covering the editor step by step, and it is linked from the [PUBG section on CurseForge](https://www.curseforge.com/pubg-battlegrounds).

Publishing your own mode puts it in the same catalogue as everything else here, and the official contests are open to new creators.

## Troubleshooting
**F10 does nothing.** You are probably not in a UGC Alpha Map room. The file loader only exists in that mode, not in a normal custom match.

**The file loader opens but my mod is not listed.** Wrong folder. It has to be in `%localappdata%\TslGame\Saved\UGC`, not in the Steam install folder and not in Documents.

**The `UGC` folder does not exist.** Create it yourself at that exact path.

**The mode loads but plays wrong.** Some older `.pugc` files were built against earlier versions of the editor and have not been updated. Check the mod's **Updated** date and its comments on CurseForge.

**Friends cannot join my room.** That is a custom match problem rather than a mod problem. Check the room settings and that everybody is on PC.

**Can I use these in ranked or normal matches?** No. UGC content only exists inside custom matches, by design.

**Am I going to get banned?** Not for this. You will be banned for client-side modifications, which is a completely different thing. Stick to `.pugc` files from CurseForge.

## Conclusion
PUBG modding boils down to three steps: download a `.pugc` from CurseForge, drop it in `%localappdata%\TslGame\Saved\UGC`, and load it with F10 inside a UGC Alpha Map custom room. Only the host needs the file.

The important part is the part that is not in those three steps. PUBG is an anti-cheat protected competitive shooter, and the UGC system is the entire legitimate modding surface. Anything promising more than that is a cheat and will cost you your account.

For the games that do need a mod manager, the [TMC App](https://github.com/modcommunity/tmc-app) is ours. It is open source and very early in development, and feedback on it would be appreciated.

## See Also
* [PUBG: BATTLEGROUNDS on CurseForge](https://www.curseforge.com/pubg-battlegrounds)
* [Official PUBG Discord](https://discord.com/invite/battlegrounds)
* [PUBG Wiki](https://pubg.wiki.gg/)
* [PUBG on Steam](https://store.steampowered.com/app/578080/PUBG_BATTLEGROUNDS/)
* [TMC App](https://github.com/modcommunity/tmc-app)

We keep this guide as up-to-date as we can, but PUBG's UGC system is still developing and menus change with it. If an instruction here no longer matches what you are seeing, please report it or open a [pull request](https://github.com/modcommunity/how-to-install-mods-in-pubg/pulls) on this guide's GitHub repository.

Join our [Discord server](https://discord.moddingcommunity.com) if you have any questions or want help with anything modding related!
