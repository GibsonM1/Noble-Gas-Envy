# Noble Gas Envy: Card Lab

Make-up version of the Ch5 Noble Gas Envy ion cards (Part I + Part II H/O `110922`). It's a class interactive built for Chromebooks at 1366×650. Guest mode only: work saves on the device, and at the end SS copy their answers into Google Classroom and show the Finished screen.

Live URL once pushed: `https://gibsonm1.github.io/Noble-Gas-Envy/`

## What SS do

1. **Make cards** (default 6: Na, O, Mg, C, Cl, Ar). Each card has 4 steps:
   - Protons: enter p⁺. Neutrons are filled in for SS (`ASK_NEUTRONS`).
   - Arrange electrons: shade seats (blue electrons) on the same energy-level template as the paper card.
   - Noble gas envy: circle loses / gains / shares / no change, then click electrons out (X + arrow) or into empty seats (arrow in). The arrows curve out to the side edge of the card, never down toward the words. Choosing **shares** (4A) finishes the card, and the bottom reads "Shares 4 e⁻ in covalent bonds. Does not form an ion."
   - Write the ion: pick one charge tile, from 4− to 4+ (0 = no charge). 1+ shows as Na⁺ on the card. The charge spot on the card is highlighted. Cations show in red/pink and anions in blue, matching the counter.
   - The **p⁺/e⁻ counter** pairs every proton with an electron. The leftovers are highlighted in yellow, the same as the charge spot on the card, for the first 2 cards (`HIGHLIGHT_COUNTER_CARDS`). The counter hides itself after 3 first-try charges, and SS can reopen it.
2. **Check team.** The other 14 cards arrive "made by tablemates." 3 of them hold mistakes taken from real student work:
   - P⁻ for P³⁻ (charge number)
   - S²⁺ for S²⁻ (sign)
   - Ca⁺² (order)
   - SS find each mistake, pick the reason, and fix the card. False alarms are counted.
3. **Find patterns.** Part II Q1–4, Making Sense, the Sb³⁻ question, and the "same electrons as S²⁻" question. The finished mini PT stays on screen the whole time.
4. **Finish.** A review with edit links, then the Finished screen with name, period, timestamp, first-try count, and hints used, plus a **Copy my answers** button.

## Teacher settings (CONFIG block at the top of the script)

| Setting | Default | What it does |
|---|---|---|
| `CARDS_TO_MAKE` | 6 | Cards the student makes alone. 20 = whole set, which skips the team check |
| `CARD_ORDER` | Na, O, Mg, C, Cl, Ar, Al, P… | Which cards come first |
| `TEAM_MISTAKES` | 3 | Planted mistakes (0 = skip the team check) |
| `ASK_NEUTRONS` | false | true = students calculate n⁰ like on paper |
| `HIGHLIGHT_COUNTER_CARDS` | 2 | Cards that get the yellow highlight on unmatched particles |
| `FADE_COUNTER_AFTER` | 3 | Hides the counter after this many first-try charges (0 = never) |
| `FILL_SHORTCUT_AFTER` | 1 | Turns on the "Fill inner energy levels" button after N finished cards |
| `WRONG_TRIES_BEFORE_ANSWER` | 2 | Wrong tries allowed before the answer is shown |
| `INCLUDE_EXTENSION` | true | Includes the Sb and S²⁻ questions |

Changing `CARDS_TO_MAKE` doesn't affect a student who has already started on that device. To reset, they use **Start over** on the start screen.

## Alignment (teacher-facing)

- **PE:** HS-PS1-1 ✓ (SFUSD places it in Ch5 for predicting ions from PT patterns)
- **SEP 2, Developing and using models:** the shell model and the p⁺/e⁻ pairing counter
- **SEP 7, Engaging in argument from evidence:** in the team check, SS name what's wrong and fix it, using the counter as evidence
- **CCC 1, Patterns:** the ion PT and the Part II pattern questions
- **Flags:**
  - B³⁺ is accepted to match the class pattern table (3A loses 3). Real boron shares. ⚠ beyond the NGSS assessment boundary
  - Hydrogen accepts both H⁺ (loses 1) and H⁻ (gains 1)
  - Sb (Q6) is period 5, outside the 1–20 card set

## Test on a real Chromebook

- Seat clicking with the trackpad. Seats are about 27 px wide, smaller than the usual 48 px target, to keep the paper layout.
- Uses the shared `theme-v1.css` classes (md-btn, md-stepper, md-top-app-bar, etc.) like Decay-Series. It was tested with the real theme file, and fallback styles are built in. Hints use amber, not red, because red/pink means + charge.
- **Copy my answers** → paste into Classroom.
- Close the tab, reopen it, and check that **Continue** resumes the work.

Version: Nov 8, 2026, update 3
