# Morsey — CW Morse Trainer

A single-file, zero-dependency web app for learning to copy Morse code (CW) by ear. Open it in any modern browser — no build step, no install, no network required. Progress is saved locally.

**Live demo:** https://abperiasamy.github.io/morsey/ (enable GitHub Pages to activate)

## Features

- **Learn mode** — tap any key to instantly hear its CW code and see the dits & dahs, so you can explore the alphabet at your own pace.
- **Progressive drills** — letters (Koch order), numbers, symbols, and a mixed set. New characters unlock automatically as your streak grows.
- **Ham-radio practice** — random callsigns, common words & Q-codes, and full QSO phrases (`CQ CQ DE W3AB`, `UR RST IS 599`, …).
- **Realistic audio** — 600 Hz sine tone generated with the Web Audio API, with proper dit/dah/character timing.
- **Adjustable speed** — 5–35 WPM character speed, plus Farnsworth (QRS) spacing to slow the gaps while keeping characters crisp.
- **On-screen + physical keyboard** — type your answer, use `Hint` to reveal the pattern, or `Replay` to hear it again.
- **Stats & persistence** — streak, accuracy, correct count, and pool size; all settings and progress persist in `localStorage`.
- **CW reference chart** — full letters/numbers/symbols lookup, one tap away.
- **Mobile-first** — responsive layout tuned for phones through desktop.

## Usage

Just open `morsey.html` in a browser. That's it.

```sh
# or serve it locally
python3 -m http.server
# then visit http://localhost:8000/morsey.html
```

### Modes

| Button | Mode |
| --- | --- |
| **Learn** | Tap keys to hear codes; no scoring |
| **ABC** | Letters, Koch teaching order |
| **123** | Numbers |
| **Sym** | Punctuation & prosigns |
| **Mix** | Letters + numbers combined |
| **Calls** | Randomly generated callsigns |
| **QCodes** | Common CW words & Q-codes |
| **QSO** | Full on-air phrases |

### Keyboard shortcuts

| Key | Action |
| --- | --- |
| Letter / number / symbol | Answer the current prompt |
| `Space` | Replay the code (or word/sentence separator in QSO mode) |
| `` ` `` or `~` | Toggle hint |
| `Tab` | Cycle to the next mode |
| `Esc` | Close the reference chart |

## Tech

Plain HTML, CSS, and vanilla JavaScript in one file. Audio via the Web Audio API; state via `localStorage`. No frameworks, no dependencies, no backend.

## License

GPL-3.0-or-later. Copyright (C) 2026 Anand Babu Periasamy ([@abperiasamy](https://x.com/abperiasamy)). See the license header in `morsey.html` and https://www.gnu.org/licenses/gpl-3.0.html.
