# Numerology Chart

Type a name, get its numerology number. That is the whole tool.

**Open it here: https://balaji4aws.github.io/numerology-chart/**

Works on a phone or a computer. Nothing to install, and nothing you type leaves
your device.

## How to use it

1. Open the page.
2. Type a name in the box.
3. Press Enter or tap **Calculate**.
4. Type another name and do it again.

The page shows the name you typed and its total, and adds it to a list of the
names you have checked, so you can compare a few side by side.

Each row has a ✕ button if you only want to drop that one name. Tap **Clear**
to empty that list and start over. Refreshing the page empties it too. Nothing
is saved anywhere, so once the list is gone it is gone.

## How the number is worked out

Every letter is worth a number from 1 to 8. Add up the letters of the name.

| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|
| A | B | C | D | E | U | O | F |
| I | K | G | M | H | V | Z | P |
| J | R | L | T | N | W |   |   |
| Q |   | S |   | X |   |   |   |
| Y |   |   |   |   |   |   |   |

Example: `RAM` = R(2) + A(1) + M(4) = **7**

A few things worth knowing:

- There is no 9. This is the Chaldean chart, which leaves 9 out.
- Capitals do not matter, so `ram` and `RAM` both give 7.
- Spaces, numbers and punctuation add nothing, so you can type a full name in
  one go.
- The same chart is printed at the top of the page, so you can check a letter
  by eye.

## For developers

Everything lives in `index.html` — markup, styles and the calculation in plain
JavaScript. No build step, no dependencies. Open the file in a browser, or serve
the folder:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
# then visit http://127.0.0.1:8000
```

The live site is published with GitHub Pages from the root of the `main` branch,
so pushing to `main` redeploys it within a minute or so.
