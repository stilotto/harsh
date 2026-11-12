# Harsh — design notes

## The problem
Day one of a survival game is tense because you have nothing and the sun is setting.
That tension fades because safety *accumulates*: walls, farms, chests. Once you
have a base, night is no longer a question.

## The answer: safety never accumulates
Every rule exists so that each dusk asks the same question day one asked.

| Pillar | Rule |
| --- | --- |
| You can't stay | The Frost advances from the west (fast by day, slow by night) and swallows everything: camps, trees, fires. |
| You can't stockpile | Carry at most 10 wood and 10 berries. Nothing regrows. |
| Light is temporary | Fires burn down whether you use them or not. Torches last ~35 s. A windbreak halves burn rate but stays behind when you leave. |
| It gets harder | Nights grow longer, the Frost speeds up, the land thins out, shades get faster and more numerous. |
| Night is a real threat | Darkness chills you; shades hunt you and only light pushes them back. |

The core daily decision: **how far east do I push before I stop to camp?**
Too close to the Frost and it reaches your fire by morning. Too far and you are
gathering in the dark.

## Making it fun: every resource has three uses, every night has verbs
Wood is fuel, torch and weapon, and you still only carry 10.

| Addition | Why |
| --- | --- |
| Thrown brands (Q, 1 wood) | An active answer to shades. Bursts where it lands; kills can drop charcoal, so a good throw pays for itself. |
| Frost moths (night 2+) | They eat the fire, not you. Stand in their path to swat them, so you move inside the light. |
| Hollows (night 3+) | Light only burns them slowly. A big fire, a brand, or kiting through the light. |
| Gusts (night 2+) | Unsheltered fires burn 3x for a few seconds. Makes the windbreak a real choice. |
| Moonblooms | Heal, but they open out in the dark. A reason to leave the fire. |
| Frost surges (day 2+) | One telegraphed lunge per day, so the Frost is never a solved timer. |
| Running (Shift) | Speed for food. |
| Ruins and relics | Pick 1 of 2 every ~4 chunks. Gear travels with you; safety still does not. |
| Sound and feedback | Synthesized wind, crackle, chops, banners, floating numbers. |

## Progression without permanence: the camp kit
Safety still never accumulates in a place. It accumulates in your pack, and it wears out.

- Camp pieces are built from wood and stone (rocks are now gatherable), set at dusk and packed up at dawn with Space.
- Every piece has wear that travels with it: Stakes 4 hits, Windbreak 3 nights, Ember trap 3 bursts, Cairn lamp 150 s of light, Sentinel 12 shots.
- New pieces are learned by surviving: Stakes and Windbreak day 1, Ember trap day 2, Cairn lamp day 3, Sentinel day 5.
- The pack holds 3 pieces on day 1 and grows to 7. What you cannot carry, or do not pack in time, the Frost takes.
- From night 2, shades telegraph (red eyes) and rush through the light, so a fire alone stops being enough.
  A big fire burns a rusher down; stakes, traps and sentinels cover the rest.

## Tuning knobs (top of `index.html`)
`DAY_LEN`, `nightLen`, `frostSpeed`, `fireR`, `cap`, `RELICS`, spawn timers in `update`, chunk density in `genChunk`.

## Ideas to try next
- Rain that soaks wood. A map relic that marks caches.
- Other survivors' cold campfires left behind (ghost runs).
