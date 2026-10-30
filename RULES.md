# MLP Card Game rules reference

Last verified against KAYOU's official rules page and Hearth’s Warming Eve gallery on **October 29, 2026**. The currently linked document is **My Little Pony Card Game Comprehensive Rules v1.3.0**. The rules + AI companion covers SD01, BP01, BP02, BP03, and BP04.

When authorities conflict, KAYOU rule 101.1.0 gives priority to an official **Card Paraphrase/Q&A**, then the **printed card ability**, then the **comprehensive rules**.

## Decks and setup

- Main Deck: exactly 50 Character, Event, and Item cards.
- Scene Deck: exactly 15 Scene cards.
- Story Deck: four Story cards with the same Main Title, different Subtitles, and stages I–IV.
- Main Character: exactly one.
- A deck may contain at most four copies of one collector ID. An Everyday Scene may appear in any quantity.
- Randomize both decks and determine the first mover.
- Each player draws five cards. The first mover decides first whether to take their single allowed mulligan, then the rival decides. A mulligan puts the entire hand on the Main Deck's bottom in any chosen order and draws five replacements.
- After mulligans, place the top four Main Deck cards face down as Plans on Story stages I–IV.
- The first mover places one Scene face down and untapped. The rival places one Scene face up and untapped.

## Public and private information

- Adventure and Retirement Areas are public. Characters, Items, Stories, and Main Characters can be inspected.
- Plans and both decks are face down and private. Players may check how many cards remain in either deck but not their order or identity.
- A player may inspect their own Hand. A rival may check the number of cards in that Hand, but not their identity.
- The Scene Area is public (305.1.0). Both players may inspect its Scene cards even when face down. Inspection does not turn the Scene face up, untap it, or restore its Inspo Boost. Cards still in the Scene Deck remain private.

## Turn sequence

1. **Starting Phase:** untap all of the active player's Characters and Scenes; draw one card except on the first turn; add the Scene Deck's top card face up and untapped; resolve beginning-of-turn effects.
2. **Main Phase:** the active player may play Characters, Events, and Items or use legal activated abilities in any order while no effect is pending.
3. **Contact Phase:** skip this phase on turns one and two. Otherwise resolve the physical lanes in the first mover's Left, Center, Right order.
4. **End Phase:** end every until-end-of-turn effect, then the active player chooses and discards down to ten cards.

The offline app shows all four steps above every match. Completed steps are marked, the current step is highlighted, and the explanation changes when Harmony, targeting, Inspiration Boost, Contact, or End-Phase discard choices are pending. The log records Starting Phase untaps, the draw, the added face-up Scene, and each later phase boundary. End Phase is not available until Contact has finished resolving.

## Main Phase and Harmony

- To play a card, choose and tap exactly as many untapped Scenes as its final Harmony cost.
- A face-down Scene still produces Harmony. Turning a Scene face down and tapping it are separate actions and states.
- A Character needs an empty Adventure Slot. Its Appear ability triggers after it enters the Adventure Area.
- An Item must have a legal Character to adorn. A Character may have one Item; playing a new one retires the old one first.
- An Event enters the Resolution Area, resolves its printed actions in order, then enters the Retirement Area.
- Rule 502.1.2 allows ordinary Events and abilities even if their effects cannot be performed; resolve as much as possible. Costs and explicit use conditions must still be satisfied. Inspo Boost and Explore are exceptions: they cannot be used if no part can be performed.
- A `[Tap]` activated ability is usable only during its controller's Main Phase, while no effect is pending, and only if its Character is untapped. Tapping is paid before the effect resolves.

## Contact

- Two Characters in opposing Slots Contact. First, the active player may repeatedly turn down one applicable face-up Scene at a time for Inspiration Boost, then passes. The rival does the same. A tapped face-up Scene is still eligible; turning it down does not untap it or tap it, and it remains face-down afterward unless a card effect turns it face-up.
- Calculate final Inspiration from the printed value plus every active continuous, Item, temporary, and Scene modifier. Inspiration cannot be less than zero.
- The lower-Inspiration Character loses and retires. On a tie, both Characters lose and retire. The active player's Area Transfer is processed before the rival's.
- A protected Character or an Item with a valid replacement effect follows its printed rule instead of the normal Contact retirement.
- If only the active player has a Character in the lane, its controller chooses exactly one legal action: **Promote**, **Intervene**, or **Skip**.
- Promote advances the active player's Main Character one Story stage. A rival Plan on the matching next stage blocks promotion. Resolve the promoted Story ability; reaching stage IV wins immediately as a rule action.
- Intervene removes the rival's lowest-stage Plan. Reveal it. If it has a Pre-plan ability, resolve it and retire that Plan; otherwise add it to its owner's Hand.

## Abilities and resolution

- **Triggered abilities** such as Appear, Farewell, Pre-plan, end-of-turn, movement, Plan-removal, and Intervene triggers are mandatory when their conditions are met.
- **Continuous abilities** and conditional Harmony/Inspiration modifiers update whenever their condition becomes valid or invalid.
- **Activated abilities** are player actions with a cost. The companion exposes every currently legal activation to both human and AI controllers.
- Resolve multiple actions in the exact printed order. Draw and discard multiple cards as one action; the player chooses discards and any required order.
- If simultaneous triggered abilities share one controller, that controller chooses their resolution order. When both players have simultaneous triggers, use the official active/rival pending-resolution order.
- Events, resolving Pre-plan cards, and retiring Characters with Farewell effects remain in the Resolution Area until their pending effects finish.
- Human players receive explicit choices for Harmony payment, targets, discards, movement Slots, revealed cards, deck/Plan order, simultaneous abilities, Inspiration Boosts, and Contact actions. AI players resolve the same choices through the same legality engine.

## Verified digital-play examples

The following interactions were checked in KAYOU's digital game on **August 18, 2026** and are regression-tested in the offline app:

- **Healthy Salad (SD01B-SPR03):** pay 4 Harmony, give every `[Pet]` in your Adventure Area +2 Inspiration until end of turn, then move the Event to Retirement. The modifier clears during End Phase.
- **Rabbit Pocket Watch (SD01B-SPR04):** pay 3 Harmony and adorn a legal `[Fluttershy]`. It stays attached and gives that Character +1 Inspiration for every Character in its controller's Adventure Area.
- **Angel (SD01B-U04):** its printed 3 Inspiration becomes 5 during the rival's turn while a `[Fluttershy]` is in its controller's Adventure Area. This is a continuous rival-turn modifier, not a leftover Healthy Salad bonus.
- **Fluttershy (SD01B-SR01):** its Appear ability draws 1 when an `[Angel]` is already in its controller's Adventure Area.
- **Dragonshy:** stage I draws 1; stage II gives a chosen friendly Character +2 Inspiration until end of turn; stage III returns a chosen `[Pet]` from Retirement to Hand; promotion to stage IV wins immediately.

## Common card actions

- **Draw:** move the Main Deck's top card to Hand. Trying to draw while it is empty loses the game.
- **Discard:** choose a Hand card and move it to the Retirement Area. End-Phase discards do not trigger abilities.
- **Add a Scene:** move the Scene Deck's top card to the Scene Area face up and untapped unless the effect says otherwise. Tapped/untapped controls Harmony payment, while face-up/face-down controls whether its Inspo Boost remains available; these are independent states.
- **Become a Plan:** place the card face down on the highest-stage Story that does not already have a Plan.
- **Move:** use a legal empty Adventure Slot chosen by the controller. Moving into the Adventure Area triggers Appear.
- **Retire:** move the Character and its Item through the Resolution Area, resolve Farewell abilities, then place them in the Retirement Area unless an effect moved them elsewhere.
- **Reveal/Look:** show only the cards specified, make the required choices, then return or move cards to the printed destination and in the player-selected order.

## Enforced card pool

- 704 database entries: 126 Friendships Begin starter cards, 144 Fantasy Wonderland, 144 Discord!!!, 140 Nightmare Night, and 150 Hearth’s Warming Eve entries (144 deck cards plus six Present tokens).
- Every nonempty printed ability is checked against the engine's supported effect families during the automated test suite.
- Treats and six Present types are supported. Tokens are outside the decks and cannot be added in Deck Creator.
- Card Game Simulator remains a manual tabletop sandbox. Automatic legality and AI enforcement are provided by the local rules + AI companion.

## Nightmare Night: Treats and Scenes

- A Character can have **at most one Treat**. Putting another on it does nothing and does not trigger a placement bonus. The on-card 🍬 Treat marker shows its current state.
- Treats have no built-in Inspiration bonus. Individual cards grant bonuses for having, receiving, or removing a Treat. Wording such as “has had a Treat” checks whether it currently has one, not whether it had one earlier.
- Treats remain when a Character taps or Moves between Adventure slots, and accompany it into the Resolution Area. They are silently cleared when it leaves Adventure/Resolution; this cleanup is not a “Remove Treat” effect.
- Some abilities spend a Treat without tapping. Rainbow Dash BP03-CR05 requires **both tap and Remove Treat**. The legal-ability buttons enforce these distinct costs.
- **Square (BP03-ER01)** is an Everyday Scene, so it may exceed four copies. It boosts a Nightmare Night Character by +1 for that Contact.
- **Market (BP03-ER02)** is not Everyday: all its artworks together are limited to four copies. Its boost puts a Treat on the Nightmare Night Character in Contact; it does not give an automatic +1.
- The six Nightmare Night built-in decks are custom showcases, not official starter products. Existing SD01 starters keep their published card quantities.

### Nightmare Night ability examples in version 3.0.0

- Twilight Sparkle BP03-CR01 spends its Treat to recover an Event from Retirement. This is not a draw from the deck. The AI saves its Treat when no Event can be recovered.
- Fluttershy BP03-CR02 gives a chosen rival Character -2 Inspiration and itself +2 until the end of turn. Follow the mirrored Contact lanes when choosing the rival; the AI includes both changes when evaluating targets.
- Mayor Mare BP03-C16 taps to give Treats to **up to two** eligible Nightmare Night Characters. You may choose fewer than two. Marked Characters cannot receive a second Treat; the AI stops after useful targets.
- Candy Bag offers two separate tap abilities: a temporary Inspiration bonus, or a Treat for a chosen eligible Character. Tapping for one means the same Character cannot immediately pay another tap cost without being untapped.
- Rafting's draw follows the Character's retirement process; it does not replace a Farewell. End-phase discards down to ten do not trigger Spike's ordinary discard reward.
- Plan cards remain private until an effect permits looking at or revealing them. Moving a Character into a Plan slot clears its Treat silently and handles its adorned Item separately.

These are explanatory examples, not new tournament rulings. Printed card abilities and official Q&A take precedence as described above. The bundled official PDF remains rules v1.3.0; **4.0.1 is the app version**, not a new KAYOU rulebook version.

## Hearth’s Warming Eve: Presents and Explore

- **BP04** adds 144 deck cards and six Present tokens, with 47 alternate prints and 24 individual landscape Story backs. Six custom Hearth’s Warming Eve decks accompany the original starters; these new decks are not official preconstructed products.
- Deliver Present places the specified token on the chosen Character. Presents give no generic bonus, and do not count as Items. Unlike Treats, the rulebook does not impose a one-Present limit.
- During Starting Phase, after untapping, drawing and adding the Scene, the active player declares every Present they want to unwrap and its order. The rival then declares theirs. Resolve the rival’s declared Presents first, followed by the active player’s. Either player may keep some or all Presents.
- Click a 🎁 marker to inspect its printed token card. When a choice requests a Present, choose the specific token in the helper or on the Character. Distinct tokens remain separate choices even when they share a name.
- Twilight’s Present reveals two, adds one to Hand and puts the rest on the bottom in chosen order. Fluttershy’s recovers a Character costing 3 or less. Pinkie’s grants +1 Inspiration until End. Applejack’s grants a tap-to-untap-Scene ability until End. Rainbow’s optionally moves its holder to an empty friendly Slot. Rarity’s gives a chosen rival Character −1 Inspiration until End.
- Presents travel with their Character between Adventure slots and into Resolution. Leaving Adventure/Resolution clears remaining Presents silently, including when the Character becomes a Plan. This cleanup does not unwrap them.
- **Explore** turns down a face-up Scene during Main; it does not tap it or spend Harmony. A tapped face-up Scene can Explore. Explore is separate from Contact’s Inspo Boost. ER03–ER05 give +1 and a chosen Present; ER06 requires a Present holder, gives +1, then unwraps a selected Present.
- ER01 and ER02 are Everyday Scenes and may exceed four copies. ER03–ER06 are limited to four copies each, counting alternate art together.
- Discard and Plan costs are paid completely before the activated effect resolves. Moving a Plan as an ability cost does not remove it through the normal Plan-removal process and does not trigger Pre-plan.
- Character ability restrictions such as Trixie’s “Only use when this Character is Adorned with an Item” restrict that ability, not playing the Character from Hand.
- Effects and triggers use the same choices for humans and AI. For simultaneous BP04 triggers, each owner chooses a complete resolution order; the rival’s triggers resolve before the active player’s.
- Mage Meadowbrook and Rarity’s Tent replace retirement, so the saved Character does not trigger Farewell. When both replacements apply, its controller chooses one.

## Current official product status

- Friendships Begin and Fantasy Wonderland list March 2026 North American release dates on KAYOU's product pages.
- Discord!!! has two North American product specifications on KAYOU's page. Version A (MLP-KP-WXSK-002A-NA) is a 12-pack box released in August 2026; Version B (MLP-KP-WXSK-002B-NA) is a 20-pack box with a release date of **TBD**. Both variants share the English card gallery used by this app.
- Nightmare Night's English gallery and both product dropdown specifications (Version A and Bundle A) are archived in the database. Its 190 prints represent 140 distinct functional cards plus 50 alternate prints.
- This rules engine covers SD01, BP01, BP02, BP03, and BP04. KAYOU's other My Little Pony collectible-card lines are not part of this TCG card pool.

Official sources:

- [KAYOU rules page](https://www.kayouofficial.com/en-US/latest-activities/8)
- [KAYOU Comprehensive Rules v1.3.0 (PDF)](https://cdn.shopify.com/s/files/1/0957/9574/0955/files/MLP_TCG_Comprehensive_Regulation_v1.3.0.pdf?v=1779849947)
- [KAYOU North American MLP TCG hub](https://www.kayouofficial.com/pages/us-pony-tcg)
- [Fantasy Wonderland product and card gallery](https://www.kayouofficial.com/en-US/series/series-2nicsllo)
- [Discord!!! product and card gallery](https://www.kayouofficial.com/en-US/series/series-ry03llcx)
- [Nightmare Night product and card gallery](https://www.kayouofficial.com/en-US/series/series-27z4pa09)
- [Twilight Sparkle starter and card gallery](https://www.kayouofficial.com/en-US/series/series-9blxjfqa)
- [Fluttershy starter and card gallery](https://www.kayouofficial.com/en-US/series/series-lopk6pq7)
- [Pinkie Pie starter and card gallery](https://www.kayouofficial.com/en-US/series/series-thjm5ibc)
- [Applejack starter and card gallery](https://www.kayouofficial.com/en-US/series/series-ycaguxpv)
- [Rainbow Dash starter and card gallery](https://www.kayouofficial.com/en-US/series/series-sg84tlwq)
- [Rarity starter and card gallery](https://www.kayouofficial.com/en-US/series/series-dqaqwobk)

BP04 source: [KAYOU Hearth’s Warming Eve](https://www.kayouofficial.com/en-US/series/series-i9q374dz).
