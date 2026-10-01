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

## Tuning knobs (top of `index.html`)
`DAY_LEN`, `nightLen`, `frostSpeed`, `fireR`, `CAP`, chunk density in `genChunk`.

## Ideas to try next
- Weather (wind gusts that shrink fire radius, rain that soaks wood).
- Rare finds that change a run: a lantern, a sled (+carry), a map of caches.
- Other survivors' cold campfires left behind (ghost runs).
- Sound: crackle, wind, the shades' breathing.
