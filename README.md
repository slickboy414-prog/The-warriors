# The Warriors – Arcade Fighter

A best-of-3 rooftop arcade fighter in a single HTML file. No build step and no dependencies.

**Play:** open `index.html` in a browser, or host it with GitHub Pages.

## Controls (PC)

| Action | Player 1 | Player 2 |
|---|---|---|
| Move | A / D | ← / → |
| Jump | W | ↑ |
| Block (hold) | S | ↓ |
| Punch | F | J / Num 1 |
| Kick | G | K / Num 2 |
| Blast (30% meter) | H | L / Num 3 |
| Super (full meter) | T | I / Num 0 |
| Pause | P / Esc | P / Esc |

On phones and tablets, touch controls appear during VS CPU and Levels matches.

**Fits any screen:** the arena takes the shape of the device. Wide phones in landscape get a wider arena with no black bars, tablets and 16:10 laptops get a narrower one, and phones held upright use a 9:16 frame (like YouTube Shorts) with the arena on top and large touch controls underneath. Rotating the device switches the layout instantly. A fight camera zooms in (up to 1.3×) when the fighters are close and pulls back to keep everyone on screen.

## Rules

- Best of 3. Winning rounds 1 and 2 ends the match.
- At 1–1 the Final Round moves to the burning arena, both fighters start with a full Super, and the clock is 60 seconds.

## Levels mode

- 50 single-player levels against the CPU, in five ranks: Rookie, Fighter, Veteran, Elite and Master.
- The CPU improves every level: it blocks more, combos, punishes misses and uses Supers more often.
- It stays at human level: it reacts to what it sees with a delay (never faster than 200 ms), never blocks everything, and still makes mistakes.
- Levels 10, 20, 30 and 40 are bosses: a Shadow fighter in the burning arena, with a little more health.
- **Levels 41–50 are zombie hordes** on a foggy quarantine rooftop. Level 41 has 3 zombies and each level adds one, up to 12 at level 50, where the last one is the Zombie King.
  - Zombies rise from the floor a few at a time (3 on screen, 4 from level 45).
  - A zombie raises its arms and its eyes turn red before it strikes, so you can block. At most 3 attack at once, and after a hit you get a short recovery so the crowd can't stun-lock you.
  - Punches and kicks hit every zombie in reach, and Inferno Wave burns through the whole line. Each kill pays +1 coin.
  - Clear the horde to win the round. If you're K.O.'d, or time runs out with zombies left, you lose the round.
- Stars: 1 for a win, 2 for a 2–0 win, 3 for a 2–0 win finishing both rounds above half health.
- Progress saves automatically (YouTube Playables cloud save, or the browser's local storage).

## Coins and shop

- Earn coins for every round you win: 10 per round, more on higher levels, +5 for a perfect round.
- Match wins pay a bonus. Clearing a level for the first time pays +25, or +75 for a boss level.
- Spend coins in the **SHOP** (main menu, level select or results screen).
- **Weapons** (per fighter) look different and give small boosts:
  - Pyro: Brass Knuckles, Magma Gauntlets, Dragon Claws
  - Valkyrie: Twin Daggers, Plasma Katana, Void Lance
- **Attire** (per fighter) is cosmetic: new colours plus hoods, capes, crowns, a winged helm, Phoenix wings or a Ghost aura.
- The shop preview shows your fighter wearing whatever you hover or tap. On touch screens, tap once to preview and tap again to buy.
- Coins, purchases and equipped gear save with your level progress.

## Daily missions

- Three new missions every day at midnight (your local time), from a pool of 13: win rounds or matches, win as a specific fighter, use Supers, hit with Blasts, land three-hit combos, block attacks, win a perfect round, win after using Rage, win with a finisher, clear levels, defeat zombies (once the zombie levels are unlocked).
- Coins pay out the moment a mission is completed. Finishing all three pays a bonus that grows with your daily streak: +50 on day 1 up to +110 from day 7.
- One free swap a day for a mission you don't like.
- Missions count in VS CPU and Levels only (not Local 2P or the tutorial), so they can't be farmed.
- Open them with **MISSIONS** on the main menu; the badge shows today's progress (for example 1/3).

## YouTube Playables

The page loads the YouTube Playables SDK and handles pause, resume and the audio toggle. Outside YouTube it runs as a normal web page.

## Improvements from fighting-game research

- **Input buffer:** a button tapped up to 8 frames before you can act is remembered and fires the moment you recover, so fast taps are never lost.
- **Interactive tutorial** (TUTORIAL on the main menu): 8 guided steps against a training dummy covering move, punch, kick, block, Blast, Super, Rage and the finisher. Pays +50 coins the first time; the button shows a NEW badge until you finish it.
- **Rage mode** (R / U / RAGE button): below 30% health, once per round, 8 seconds of +30% damage and +15% speed with a red aura. The CPU uses it too from level 5, reacting faster on harder levels.
- **Signature finishers** on the match-winning K.O.: Pyro's *Phoenix Finish* and Valkyrie's *Thousand Cuts*.
