# reciteright-prototype

A prototype of the ReciteRight "Read from Quran" screen. The child reads the verse aloud, each word highlights as it's recognised, and wrong or skipped words are listed with the expected word beside what was said.

## What's here

- `index.html` is the whole prototype: one page, no build step.
- It currently uses the browser's built-in speech recognition (Chrome recommended).

## How to open it

1. Go to the repository's **Settings > Pages**, choose the `main` branch, and save.
2. GitHub gives you a web address for the page. Open it in Chrome on your phone or computer.
3. Tap **Start reciting** and allow microphone access.

## Planned next steps

- Replace the browser's speech recognition with the Quran speech model, which runs on a Colab server.
- Add a box on the page for the server address, since it changes each time the Colab session restarts.
- Add vowel (harakat) checking, once the model's vowel output has been tested.

## Notes

- Nothing in this repository contains secrets or API keys. The Colab server address is entered on the page, not stored in the code.
