# MLP Card Game — Downloads

Public compiled releases maintained by **RyogaTwo**. This repository contains release downloads, checksum files, rules, and usage notes.

## Version 4.0.1

| Platform | Download | SHA-256 |
| --- | --- | --- |
| macOS Universal — app ZIP | [MLP-Card-Game-Offline-4.0.1-macOS-Universal.zip](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-4.0.1-macOS-Universal.zip) | [Checksum](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-4.0.1-macOS-Universal.zip.sha256.txt) |
| macOS Universal — DMG installer | [MLP-Card-Game-Offline-4.0.1-macOS-Universal.dmg](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-4.0.1-macOS-Universal.dmg) | [Checksum](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-4.0.1-macOS-Universal.dmg.sha256.txt) |
| Windows x64 — portable ZIP | [MLP-Card-Game-Offline-4.0.1-Windows-x64.zip](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-4.0.1-Windows-x64.zip) | [Checksum](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-4.0.1-Windows-x64.zip.sha256.txt) |
| Windows x64 — installer | [MLP-Card-Game-Offline-Setup-4.0.1-x64.exe](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-Setup-4.0.1-x64.exe) | [Checksum](https://github.com/ryogatwo/mlp-card-game-releases/releases/download/v4.0.1/MLP-Card-Game-Offline-Setup-4.0.1-x64.exe.sha256.txt) |

Mac packages support Intel and Apple silicon on macOS 13 or later and are Developer ID signed and Apple notarized. Both the Windows installer and the game EXE have verified timestamped signatures. Extract the entire Windows portable ZIP before running the app.

Both players must use version 4.0.1 for LAN play.

[All releases](https://github.com/ryogatwo/mlp-card-game-releases/releases)

[Read the rules reference](RULES.md)

## About the game

An unofficial, personal-use implementation of KAYOU's My Little Pony Trading Card Game using the six North American Friendships Begin starter decks and four booster pools:

- SD01 — Friendships Begin starter decks
- BP01 — Fantasy Wonderland
- BP02 — Discord!!!
- BP03 — Nightmare Night
- BP04 — Hearth’s Warming Eve

The project has two deliberately separate play surfaces:

1. **Card Game Simulator module** — the tactile tabletop experience inside the separately installed Steam game.
2. **Rules + AI companion** — a local browser game for Human vs AI, AI vs AI, local Human vs Human, and two-computer LAN play.

This split is necessary because Card Game Simulator's public custom-game format defines cards, decks, zones, boards, and setup, but exposes no rules-scripting or bot API. The companion uses the same card/deck database and performs automated turns without changing or automating Steam itself.

## Hearth’s Warming Eve update · 4.0.1

Adds 144 BP04 deck cards, six Present tokens, 47 alternate prints, four product specifications, and six custom decks from the [official Hearth’s Warming Eve gallery](https://www.kayouofficial.com/en-US/series/series-i9q374dz). Delivery, unwrap choices, upkeep order, Explore, triggered abilities, discard/Plan costs and retirement replacements share the human/AI engine. See BP04 audit and playtest report (bundled with the offline app). Version 4.0.1 requires the same version on both LAN peers. See release notes (bundled with the offline app) for the packaging and verification checklist.

## Nightmare Night update — 3.0.0

Adds 140 functional BP03 cards, 50 alternate prints, individual Story backs, Treat mechanics, six custom Treat showcase decks, and updated offline help. The AI uses mirrored lanes, avoids the identified wasteful Treat activations, and improves Fluttershy's target choices. Both platforms use the expanded card pool. LAN compatibility requires matching versions. See 3.0.0 release notes (bundled with the offline app) and AI verification (bundled with the offline app).

## Standalone offline Swift app

Double-click **MLP Card Game Offline.app** for the self-contained macOS version. Version 4.0.1 is a native SwiftUI/WebKit application with its own Swift local server, 704 library entries and their local English artwork, alternate art, official card backs, updated rules, illustrated guide, offline community wiki, 26 decks, animated AI playback, LAN play, and Card Game Simulator module bundled inside. It does not require Node, a Terminal window, an external web browser, or an internet connection during play.

The play screen shows one action at a time, including payments, card movement, abilities, Contact and promotion. Computer opponents proceed automatically; use **Pause AI**, playback speed, **Reduce motion**, or **Finish animation** to control the presentation. See 1.8.4 release notes (bundled with the offline app).

Version 4.0.1 retains the audited card-effect, partial-resolution, Plan-card conservation, reveal-timing and immediate-win fixes from 2.0.1. LAN matches require the same installed version, including 4.0.1 on both computers. Lobby chat, deck locking, and previous playfield improvements remain available.

The app is a Universal 2 build for both Apple Silicon and Intel Macs and requires macOS 13 or newer.

Custom decks and generated CGS files are kept in `~/Library/Application Support/MLP Card Game Offline/`. Use **Install CGS** in the native toolbar while Card Game Simulator is closed to copy the bundled module into CGS, or **Steam Simulator** to launch the installed Steam game.

## Standalone offline Windows app

The Windows edition provides the same simulator, rules engine, AI modes, deck creator, card library, local English images, alternate art, card backs, guide, and CGS module in a portable Electron application for 64-bit Windows 10 and Windows 11. It includes its own browser runtime and does not require Node.js, Edge WebView, or internet access during play.

Use the signed **MLP Card Game Offline Setup** installer for a standard Windows installation with desktop and Start Menu shortcuts, install-location selection, and an uninstall entry. The portable ZIP remains available; extract it completely, then run **MLP Card Game Offline.exe** without separating it from its `resources` folder. Custom decks are stored under `%APPDATA%\MLP Card Game Offline`. The Windows **Install CGS** button uses Card Game Simulator's documented Steam folder at `%USERPROFILE%\AppData\LocalLow\Finol Digital LLC\Card Game Simulator\games`; quit CGS before installing.

## LAN play

Use **LAN Play** on two offline apps connected to the same home or private local network. Each person enters a name, chooses a legal built-in or custom deck, and clicks **Enter lobby**. Select the other visible player and click **Challenge**; the challenged player must explicitly accept before the match starts. macOS may ask for Local Network access, and Windows Firewall may ask to allow the app on private networks.

During a match, the guest sends a private LAN heartbeat every 1.5 seconds. If either app cannot confirm the other player for six seconds, both game actions and choices are paused and a red **Disconnected** notice appears without erasing the match. The notice clears automatically after the connection returns.

The apps exchange each selected deck, seed, seats, and legal action journal directly over the LAN, so Mac-to-Mac, Windows-to-Windows, and Mac-to-Windows matches use the same deterministic rules engine. Each screen shows only its own hand and private card choices. A one-way 24-character machine ID is derived from the active adapter's MAC address; the raw MAC address is never displayed or broadcast. Lobby advertising stops after leaving the lobby or starting a match, and no internet service or account is used.

## Current reference status

Last verified against KAYOU's official North American pages on **October 29, 2026**:

- KAYOU's rules page still serves **My Little Pony Card Game Comprehensive Rules v1.3.0**.
- Official authority order is Card Paraphrase/Q&A, then printed card ability, then the comprehensive rules.
- Friendships Begin and Fantasy Wonderland list March 2026 releases. Discord!!! has two North American product specifications on the same official page: Version A is a 12-pack box released in August 2026, while Version B is a 20-pack box whose release date remains **TBD**. Both variants use the same published English card list.
- This app deliberately covers the SD01, BP01, BP02, BP03, and BP04 TCG pool only; other KAYOU My Little Pony collectible-card lines are separate products.

## What is included

- 704 database entries (698 deck cards and six Present tokens): all 126 cards required by the six Friendships Begin starters, plus 144 Fantasy Wonderland, 144 Discord!!!, 140 Nightmare Night cards, and 150 Hearth’s Warming Eve entries. Parallel/alternate-art prints with duplicate collector IDs are intentionally deduplicated.
- All 386 Character Inspiration values are included and checked against the official English card faces.
- Official English KAYOU card scans are stored locally for the complete 704-entry pool. All titles, printed character lines/traits, Harmony costs, Inspiration values, and rules text entries were audited against those card faces; the 288 BP01/BP02 booster entries were retranscribed from the printed cards instead of retaining the earlier machine translations.
- English-only local artwork: 704 base entries plus 229 locally cached parallel, promo, and day/night alternate-art printings for 171 cards. The Discord base set and 94 set alternates published on the official [Fantasy Wonderland](https://www.kayouofficial.com/en-US/series/series-2nicsllo) and [Discord!!!](https://www.kayouofficial.com/en-US/series/series-ry03llcx) galleries are cached from KAYOU's English files; English promo and starter variants use the reference archive as a fallback. Six Japanese-only Discord promo variants are intentionally omitted.
- Twenty-six legal decks: six Hearth’s Warming Eve showcases, six Nightmare Night Treat showcases, all six complete Friendships Begin starters, one BP01 + BP02 showcase for each Mane Six Main Character, and Twilight Sparkle and Applejack test builds.
- Correct 50-card Main Deck, 15-card Scene Deck, four-stage Story, and one Main Character stacks in CGS.
- A two-player playmat with three Adventure lanes, Story/Plan, Scene, Main Character, Main Deck, and Retirement areas.
- Deterministic AI with seeded matches, Harmony-aware play selection, activated abilities, target/discard/order choices, mirrored lane/contact evaluation, Plan intervention, Story promotion, and every printed effect family in the included card pool.
- Automated card-data and effect-family checks plus behavioral rules regressions, deck legality, official setup and phase rules, player choices, Resolution Area timing, simultaneous triggers, and repeated AI-vs-AI match completion.

## Play in Card Game Simulator

Quit Card Game Simulator, use **Install CGS** in the offline app, then open Card Game Simulator:

1. Select **MLP Card Game**.
2. Choose **Single-player** for a local tabletop or **Multi-player** for another human.
3. Load **Twilight Sparkle — Test Build**, **Applejack — Test Build**, any `Friendships Begin Starter`, or any `Two-Set Showcase` deck.
4. Accept the five-card opening hand.
5. The game creates separate stacks containing 50 Main, 15 Scene, four Story, and one Main Character card.

CGS is a tabletop sandbox: players manually flip, tap, drag, draw, and resolve printed effects. Use the companion when you want enforced rules or a computer opponent.

## Opening a match

Use **Play** in the offline app to open match setup. Start a match, Deck Creator, and Card Library have collapse controls. **New match** appears only after cards are dealt; it discards the current in-memory match, expands setup, and waits for another click on **Deal opening hands**.

## Create or edit decks

Click **Deck Creator** in the offline app to open the local deck workshop. You can start with an empty deck or duplicate any included deck, then search all 698 deck cards, filter by release or type, and add or remove cards with their local English images visible.

Built-in decks are protected as read-only. Duplicate one to make an editable custom copy. The live validator checks the 50-card Main Deck, 15-card Scene Deck, four matching Story stages, one Main Character, card-copy limits, and all other construction rules. Incomplete work can be saved as a draft, but only legal custom decks appear in match setup or a generated Card Game Simulator module.

Use **Save custom decks** to keep changes on your computer. Use **Save + build CGS files** when a legal deck is ready for Card Game Simulator, then quit Card Game Simulator and click **Install CGS** in the offline app. The editor also supports JSON import and export for sharing or keeping a portable copy. Custom deck data is stored in the platform-specific app support folder described above.

## Play against the AI

The Play screen uses a compact mirrored table: each player's Adventure lanes face the opponent, with Story/Plan and Scene rows behind them. Your hand stays on your side during computer turns. Click a hand card to read its full text and legal actions; click a highlighted Adventure slot or drag a Character/Item onto it to play. Then click the highlighted Scene cards to pay the exact Harmony cost. Events use the selected-card action button. Card targets and discard choices can be selected directly on the table or in the choice panel below it. Ambiguous choices keep explicit buttons.

Blue outlines indicate legal plays or choices; gold marks the selected card. The opponent's Right lane faces your Left. The compact layout preserves all three lanes and four Story stages on narrow screens. Starting-phase untap/draw/Scene steps remain automatic in this app, unlike the separate taps in the official phone game.

Click **Play** in the offline app, then choose a mode, first-player method, and two decks. After the opening-hand mulligan decisions, use the play and ability buttons during Main Phase. A persistent four-step strip shows Starting, Main, Contact, and End; the highlighted step and explanation show what is resolving now. The choice panel handles Harmony payment, targets, discards, empty-slot movement, revealed-card selection, Plan/deck ordering, Inspiration Boost, and Contact actions. Contact must finish before End Phase becomes available. In AI vs AI mode, use **Run AI turn** to observe one complete turn or **Run AI match** to finish immediately.

An August 18, 2026 parity play-through against KAYOU's digital client confirmed the interaction and timing used here: Events are paid for, resolved, and retired; Items adorn a selected legal Character; temporary Inspiration clears in End Phase; rival-turn continuous Inspiration immediately recalculates after the active player changes; Contact resolves Inspiration Boosts before comparing the opposing Characters; and stage-IV promotion ends the match immediately. The Fluttershy starter regression covers Healthy Salad, Rabbit Pocket Watch, Angel (SD01B-U04), and the Dragonshy Story progression.

The companion enforces KAYOU Comprehensive Rules v1.3.0 for the SD01, BP01, BP02, BP03, and BP04 card pool included here. Human and computer players use the same legality checks and resolution engine. All printed abilities in the 704-entry pool are assigned to an enforced effect family; a regression test fails if an unknown ability form is added. Official Card Paraphrase/Q&A takes precedence over printed card text, which takes precedence over the general rulebook.

## Rules implemented

- Deck construction, opening five-card hand, first-player choice, one whole-hand mulligan in first-player order, and four face-down Plans
- One Main Character and Story stages I–IV
- First-player/second-player Scene orientation
- Starting, Main, Contact, and End phases, including a visible phase tracker, logged Starting actions, first-turn draw handling, and first-two-turn Contact skips
- Separate Scene face-up/face-down and tapped/untapped states; exact user-selected Harmony payment, including face-down Scenes
- Three physically opposing Adventure lanes resolved from the first mover's Left, Center, then Right
- Inspiration calculation, conditional/continuous modifiers, ties, retirement, protection, and equipped Item replacement
- Repeated, optional Scene Inspiration Boosts in active-player-then-rival order
- Explicit Promote, lowest-Plan Intervene, or Skip choices for each unopposed active Character
- Pre-plan, Appear, Farewell, activated, continuous, regulation, Story, Event, Item, draw/discard, reveal/search, Scene, Inspiration, Plan, return, movement, protection, and retirement effects
- Printed-order multi-action resolution, Resolution Area handling, and controller-selected order for simultaneous included triggers
- Ten-card End-phase hand limit
- Stage-IV victory and empty-Main-Deck loss

## Sources and rights

Rules and card data are derived from KAYOU's [official rules page](https://www.kayouofficial.com/en-US/latest-activities/8), [Comprehensive Rules v1.3.0](https://cdn.shopify.com/s/files/1/0957/9574/0955/files/MLP_TCG_Comprehensive_Regulation_v1.3.0.pdf?v=1779849947), [North American MLP TCG hub](https://www.kayouofficial.com/pages/us-pony-tcg), [Fantasy Wonderland gallery](https://www.kayouofficial.com/en-US/series/series-2nicsllo), [Discord!!! gallery](https://www.kayouofficial.com/en-US/series/series-ry03llcx), and KAYOU's six official Friendships Begin starter galleries. The exact starter quantities come from the [SD01 set list](https://kayoumylittleponycardgame.miraheze.org/wiki/SD01_set_list), while the official KAYOU card faces are the source of truth for printed titles, traits, stats, and rules wording. Official Q&A, card text, and later errata take precedence if KAYOU changes a ruling.

My Little Pony is © Hasbro. Card designs and game content are © KAYOU. Card Game Simulator is © Finol Digital LLC. This repository is an unofficial personal-play aid and is not for resale or public asset redistribution.

## Offline illustrated reference (September 3, 2026)

Use **Guide** for the illustrated how-to, or **Offline wiki** to search the bundled community reference. Both Mac and Windows builds bundle `docs/`; the Guide and Rules buttons use local pages. See the 1.8.0 release verification (bundled with the offline app) for build and test status.

The snapshot contains 1,443 article/category pages and 1,178 images (approximately 820 MiB). It credits Hope Starchild, Pony Plays Card Games and other contributors, with the full CC BY-SA 4.0 license and separate KAYOU/Hasbro artwork notices. Credits and archive limits (bundled with the offline app) identify 198 source-missing image references. Later sets/translations in the wiki do not expand the game's English SD01/BP01/BP02/BP03/BP04 pool.

## Credits

Designed By: RyogaTwo  
Unofficial App for personal use only  
**NOT FOR SALE**  
My Little Pony © Hasbro  
Cards and Artwork © KAYOU
