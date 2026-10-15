# Numerology Chart

A tiny web page that works out the numerology value of a name using the Chaldean
letter chart. Type a name, press Enter, and it shows the total.

**Live site:** https://balaji4aws.github.io/numerology-chart/

Works on phones and desktop. No app to install.

## How it works

Every letter maps to a number between 1 and 8. The page adds up the letters of
whatever you type and shows the sum, along with the name you entered.

| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|
| A | B | C | D | E | U | O | F |
| I | K | G | M | H | V | Z | P |
| J | R | L | T | N | W |   |   |
| Q |   | S |   | X |   |   |   |
| Y |   |   |   |   |   |   |   |

This is the Chaldean mapping, which has no 9 — the number 9 is treated as sacred
and left out of the letter values. The same chart is drawn at the top of the page
so you can check a letter by eye.

Example: `RAM` = R(2) + A(1) + M(4) = **7**

Letters are case-insensitive. Anything that is not A–Z — spaces, digits,
punctuation — adds nothing to the total, so first and last names can be typed
together or separately.

## Running it locally

No build step and no dependencies. Open `index.html` in any browser, or serve the
folder:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
# then visit http://127.0.0.1:8000
```

## Files

- `index.html` — the whole thing: markup, styles, and the calculation in plain
  JavaScript. Everything runs in the browser; nothing is sent anywhere.

## Hosting

The live site is published with GitHub Pages from the `main` branch. Pushing to
`main` redeploys it within a minute or so.
