# reciteright-prototype

A prototype of the ReciteRight "Read from Quran" screen. The child reads the verse aloud. The page sends short recordings to the Quran speech model, and then highlights each word as it's recognised. It lists wrong words, skipped words, and wrong vowels, with the expected word beside what was said.

## What's here

- `index.html` is the whole prototype: one page, no build step.
- `colab/quran_model_server.ipynb` loads the Quran model in Google Colab and runs a small server that the page sends recordings to.

## How to run it

1. **Start the model server.** Open `colab/quran_model_server.ipynb` in Google Colab, set the runtime to **T4 GPU**, and run the cells in order. The last cell prints a **server address**.
2. **Open the page.** Go to https://reciterightapp.github.io/reciteright-prototype/ in Chrome, on a phone or computer.
3. **Connect.** Paste the server address into the "Model server address" box.
4. **Read.** Tap **Start reciting** and allow microphone access. Read the verse aloud.

The server address changes each time the Colab notebook restarts, so you'll need to paste in the new one each time. Anyone with the address can use the server while it's running, so only share it with people testing the prototype.

## Known limits

- **Delay.** Each short recording takes a moment to process, so the highlight lags a little behind the voice.
- **Gaps between clips.** Speech during the moment between two recordings may be missed.
- **Vowel checks depend on the model.** Wrong vowels are only flagged if the model writes the vowel marks it heard. This still needs testing.
- **Extra words** added in between the verse aren't flagged yet.

## Notes

- Nothing in this repository contains secrets or API keys. The server address is typed into the page, not stored in the code.
