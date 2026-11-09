# Ordkort

Flashcards for learning Swedish vocabulary. Works in any browser, installs on your phone's home screen, and works offline.

**Open the app:** https://marthinsurya.github.io/ordkort/

## Install on your phone

1. Open the link above in your phone's browser.
2. iPhone (Safari): tap **Share**, then **Add to Home Screen**.
   Android (Chrome): tap the **⋮** menu, then **Install app** or **Add to Home screen**.
3. Open Ordkort from your home screen. After the first visit it works without internet.

## How studying works

- Tap the card (or **Show answer**) to flip it, then rate how well you knew it:
  - **Again**: you didn't know it. It comes back a few cards later in the same session.
  - **Hard / Good / Easy**: the card is scheduled for later. The buttons show when you'll see it next.
- Each word sits in a box from 0 to 7. Higher boxes wait longer before coming back:
  now, 1, 2, 4, 7, 15, 30, then 60 days.
- Levels shown in the app come from the box: boxes 0 and 1 are **❄ Hard**, 2 and 3 are **👀 Learning**, 4 and up are **🌻 Known**.
- Your original marks set where each word starts: ❄ starts in box 0, 👀 in box 2, 🌻 in box 4. Known words are spread over the first two weeks so they mix in slowly.
- **Show first** picks the direction: Swedish → English, English → Swedish, or mixed.
- **Categories** and **Levels** narrow what you study. Tap several to combine them.
- In **Word list** you can search every word, and tap a word's level to change it by hand.
- Nouns show their article in colour: *en* in blue, *ett* in red.
- If your device has a Swedish voice, a speaker button reads the word aloud.
- Keyboard on a computer: Space flips, 1 to 4 rates.

Progress is saved in the browser on each device. Your phone and computer keep separate progress, and clearing the browser's site data resets it.

## Add or change words

All words live in [`words.csv`](words.csv). Edit it right on github.com (open the file, click the pencil icon, then **Commit changes**). The live app picks up the change within a minute or two.

Columns:

| column | what to put | example |
| --- | --- | --- |
| `swedish` | the word, with *en*/*ett* for nouns | `en möjlighet` |
| `english` | the meaning; wrap it in "quotes" if it contains a comma | `"opportunity, possibility"` |
| `category` | any name; each new name becomes a filter chip | `Verbs` |
| `level` | `hard`, `learning` or `known` (starting level only) | `learning` |
| `note` | optional extra tip shown on the back of the card | `Nödvändig is more common today.` |

Progress is tied to the Swedish word, so fixing an English meaning keeps your progress, while changing the Swedish spelling starts that word fresh.

## Other flashcard apps

The [`exports`](exports) folder has the same word list for other apps:

- `swedish-words-anki.csv`: in Anki use **File > Import**. Fields are Front, Back, Tags (category and level).
- `swedish-words-quizlet.txt`: in Quizlet create a set, choose **Import**, and paste the text. Use *Tab* between term and definition and *New line* between cards.

These exports aren't updated automatically when you edit `words.csv`.

## Files

| file | purpose |
| --- | --- |
| `index.html` | the whole app (HTML, CSS and JavaScript in one file) |
| `words.csv` | the word list |
| `sw.js` | service worker that makes the app work offline |
| `manifest.json`, `icon*` | lets phones install it as an app |
| `.nojekyll` | tells GitHub Pages to serve the files as they are |

## Notes on the word list

A few entries from the original list were corrected:

- *inse* had no meaning; it's now "to realize".
- Articles fixed: *en demokrati*, *ett lösenord*, *ett bakslag*, *ett beröm*, *ett amorteringskrav*.
- Spelling fixed: *förorening* (was *förurening*).
- *beror på* is listed as the infinitive *bero på*; *en böter* is listed as *böter (pl.)*; *ett tullfilter / en tull* is *en tull*.
- Words listed twice were merged: *motsvarande*, *osäker*, *en avgift*, *en stämning*, *en gräns*.
