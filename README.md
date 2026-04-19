# Choco Crunch Clicker

A snack clicker game about covering a crunchy stack in chocolate, climbing ranks, collecting cosmetics, and showing off your battlecard.

## Development Status

This game is playable and ready to put on GitHub.

It is not Steam-ready yet. Before selling or publishing it on a big store, it should get more testing, better balancing, final art, a cleaner installer/build setup, and a proper online hosting setup. Treat this version like an early alpha build.

## Features

- Click the snack to earn points.
- The first 1,000 clicks cover the stack in chocolate.
- Ranks unlock after the chocolate is fully covered.
- Ranked tiers include Bronze, Silver, Gold, Platinum, Diamond, Mythic, Exotic, Legendary, Masters, and infinite Pro ranks.
- Pro rank turns the chocolate radioactive green.
- Pro gives 10 points per click. Other ranks give 1 point per click.
- Pro ranks get harder forever.
- Battlecard with your name, favorite chocolate color, rank, cosmetic, points, and best speedrun time.
- Shop with hats, coats, crowns, robes, capes, and rarities.
- Pro Robe is the rarest cosmetic and costs 100,000 points.
- Speedrun mode unlocks after you reach your first rank.
- Daily quests, achievements, stats, music, and sound effects.
- Optional online accounts and leaderboard through the included Node server.

## How To Play

### Windows App

Most players should use the Windows app:

```text
dist/ChocoClicker.exe
```

If you are downloading the game, keep the whole `dist` folder together. Do not move only the exe by itself.

The Windows version uses WebView2 so the game opens in its own app window.

Keep these files in the same `dist` folder:

- `ChocoClicker.exe`
- `Microsoft.Web.WebView2.Core.dll`
- `Microsoft.Web.WebView2.WinForms.dll`
- `WebView2Loader.dll`

### Browser Backup

You can also open `index.html` in a browser, but the exe is the recommended version for normal players.

## Online Accounts And Leaderboard

The game can run offline, but online accounts and the shared leaderboard need the server in the `OnlineServer` folder.

Run the server locally:

```powershell
cd ChocolatePringlesClicker\OnlineServer
npm start
```

Then open the server version in a browser:

```text
http://localhost:3000
```

To make the leaderboard work for other players, host the `OnlineServer` folder on a Node hosting service and share the hosted URL.

## Controls

- Click the snack to gain points.
- Open the shop to buy and equip cosmetics.
- Open the battlecard to view your profile.
- Start speedrun mode after you unlock your first rank.
- Use the sound menu to change music and effect volume.

## Rank Progression

Ranks begin after 1,000 total clicks.

Normal rank point requirements:

- Bronze: 3,000
- Silver: 6,000
- Gold: 10,000
- Platinum: 15,000
- Diamond: 22,000
- Mythic: 30,000
- Exotic: 40,000
- Legendary: 55,000
- Masters: 75,000

Pro starts after Masters. Pro ranks are infinite.

The first Pro rank-up needs 10,000 points, then each next Pro rank needs 1,000 more than the previous one.

## Project Files

- `index.html` - main game page
- `styles.css` - game styling and animations
- `app.js` - main game logic
- `OnlineServer/` - optional online server
- `WindowsLauncher/` - Windows app launcher source
- `dist/` - built Windows app files

## Notes

The game saves progress locally in the browser or app. If online mode is connected, account saves and leaderboard scores can sync through the server.

The dev version is separate from the normal game and is not meant for players.
