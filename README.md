# ZenithMVP — Flexbox Froggy Trainer (MVP)

A minimal, single-file Flexbox trainer inspired by "Flexbox Froggy". This project is a small educational MVP that lets users practice CSS Flexbox by editing CSS and moving a frog to a target lily pad.

- Live file: [index.html](index.html)
- Main runtime functions: [`renderBoard`](index.html), [`checkCode`](index.html), [`levels`](index.html)

---

## Demo / Run locally

This is a static HTML app. Open `index.html` in your browser or serve it with a local server:

```sh
# using Python 3
python -m http.server 8080
# or using npm + serve package
npx serve .
```

Then open http://localhost:8080 in your browser.

---

## Features

- Single-file HTML/CSS/JS implementation ([index.html](index.html)).
- Interactive UI: left panel shows the flexbox "board", right panel is a CSS editor.
- 10 levels (MVP) with incremental flexbox challenges, defined in the [`levels`](index.html) array.
- Simple "check" system that verifies user CSS against expected rules using the [`checkCode`](index.html) function.
- Responsive layout, header & footer, and a simple navigation menu.

---

## How to play

1. Open the app (see "Run locally").
2. Read the task on the right panel.
3. Enter CSS rules in the editor (the container is `#game-board { display:flex; ... }`).
4. Click "Перевірити код" to test your CSS.
   - The check logic lives in the [`checkCode`](index.html) function.
   - The app normalizes user input (lowercases + removes whitespace) before comparing with the expected string for each level.

Example:
```css
/* Type this in the editor */
justify-content: center;
```

---

## Project structure

- `index.html`
  - styles, layout, and JavaScript are implemented inline.
  - main functions and variables:
    - [`levels`](index.html) — array that defines the levels, instructions, elements, and expected CSS.
    - [`renderBoard`](index.html) — renders layout for the current level.
    - [`checkCode`](index.html) — applies and verifies user CSS against `levels[currentLevelIndex].expected`.

---

## Adding / Editing Levels

Levels are stored in the `levels` array inside [index.html](index.html). Each level entry:
```js
{
  id: <number>,
  instructions: "<string>",
  expected: "<css rule(s) expected>",
  elements: [
    { type: 'frog' | 'lily', class: 'frog'|'lily-pad', pos?: 'center'|'end'|'start' ... }
  ]
}
```

- Update the `expected` string to define what `checkCode` will match.
- Add or update `elements` to modify what appears on the `game-board`.

---

## Developer notes

- The `checkCode` function normalizes (lowercases + removes spaces) both `userInput` and `expected` before comparing.
- `gameBoard.style.cssText` is set directly and the script prefixes with `display: flex;` so only container-level flex rules are required.
- Some levels include `style` on elements to simulate fixed positions; these may be absolute positioned for particular challenges.

References:
- [`renderBoard`](index.html)
- [`checkCode`](index.html)
- [`levels`](index.html)

---

## Contributing

- This repo is a small MVP; contributions are welcome.
- Suggested improvements:
  - Add unit tests.
  - Move JS/CSS to separate files.
  - Improve input parsing & allow multiple expected rules in any order.
  - Create additional levels and polish UI translations.

---

## License

MIT License — use freely, attribute if you want.

---

## Contact

If you want improvements or help, open an issue or pull request with suggested changes.

```// filepath: c:\Users\Anwender\Desktop\flexifrogMVP\README.md
# ZenithMVP — Flexbox Froggy Trainer (MVP)

A minimal, single-file Flexbox trainer inspired by "Flexbox Froggy". This project is a small educational MVP that lets users practice CSS Flexbox by editing CSS and moving a frog to a target lily pad.

- Live file: [index.html](index.html)
- Main runtime functions: [`renderBoard`](index.html), [`checkCode`](index.html), [`levels`](index.html)

---

## Demo / Run locally

This is a static HTML app. Open `index.html` in your browser or serve it with a local server:

```sh
# using Python 3
python -m http.server 8080
# or using npm + serve package
npx serve .
```

Then open http://localhost:8080 in your browser.

---

## Features

- Single-file HTML/CSS/JS implementation ([index.html](index.html)).
- Interactive UI: left panel shows the flexbox "board", right panel is a CSS editor.
- 10 levels (MVP) with incremental flexbox challenges, defined in the [`levels`](index.html) array.
- Simple "check" system that verifies user CSS against expected rules using the [`checkCode`](index.html) function.
- Responsive layout, header & footer, and a simple navigation menu.

---

## How to play

1. Open the app (see "Run locally").
2. Read the task on the right panel.
3. Enter CSS rules in the editor (the container is `#game-board { display:flex; ... }`).
4. Click "Перевірити код" to test your CSS.
   - The check logic lives in the [`checkCode`](index.html) function.
   - The app normalizes user input (lowercases + removes whitespace) before comparing with the expected string for each level.

Example:
```css
/* Type this in the editor */
justify-content: center;
```

---

## Project structure

- `index.html`
  - styles, layout, and JavaScript are implemented inline.
  - main functions and variables:
    - [`levels`](index.html) — array that defines the levels, instructions, elements, and expected CSS.
    - [`renderBoard`](index.html) — renders layout for the current level.
    - [`checkCode`](index.html) — applies and verifies user CSS against `levels[currentLevelIndex].expected`.

---

## Adding / Editing Levels

Levels are stored in the `levels` array inside [index.html](index.html). Each level entry:
```js
{
  id: <number>,
  instructions: "<string>",
  expected: "<css rule(s) expected>",
  elements: [
    { type: 'frog' | 'lily', class: 'frog'|'lily-pad', pos?: 'center'|'end'|'start' ... }
  ]
}
```

- Update the `expected` string to define what `checkCode` will match.
- Add or update `elements` to modify what appears on the `game-board`.

---

## Developer notes

- The `checkCode` function normalizes (lowercases + removes spaces) both `userInput` and `expected` before comparing.
- `gameBoard.style.cssText` is set directly and the script prefixes with `display: flex;` so only container-level flex rules are required.
- Some levels include `style` on elements to simulate fixed positions; these may be absolute positioned for particular challenges.

References:
- [`renderBoard`](index.html)
- [`checkCode`](index.html)
- [`levels`](index.html)

---

## Contributing

- This repo is a small MVP; contributions are welcome.
- Suggested improvements:
  - Add unit tests.
  - Move JS/CSS to separate files.
  - Improve input parsing & allow multiple expected rules in any order.
  - Create additional levels and polish UI translations.

---

## License

MIT License — use freely, attribute if you want.

---

## Contact

If you want improvements or help, open an issue or pull request with suggested changes.
# ZenithMVP2
