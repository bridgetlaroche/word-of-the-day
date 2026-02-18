# Word of the Day App

## Overview
A single-file browser-based Word of the Day app (`index.html`) for collecting uncommon/literary vocabulary encountered while reading books. Hosted on GitHub Pages.

## URLs
- **Live site**: https://bridgetlaroche.github.io/word-of-the-day/
- **Repo**: https://github.com/bridgetlaroche/word-of-the-day

## How It Works
- All data stored in browser localStorage (each user gets their own collection)
- 34 seed words are baked into the HTML and loaded on first visit
- One random unseen word shown per day; tracks seen vs unseen
- No API key or backend — fully client-side

## Adding Words
- User gives Claude a list of words in chat
- Claude generates JSON with: word, pronunciation, definition, sentence, context
- User pastes JSON into the app's "Add Words" tab, or imports a .json file
- App also has a "Copy Prompt for More Words" button that builds a prompt including the user's existing collection, so Claude can suggest similar words

## Word Data Shape
```json
{
  "word": "Example",
  "pronunciation": "/ɪɡˈzæm.pəl/",
  "definition": "Detailed definition (1-2 sentences)",
  "sentence": "A vivid example sentence.",
  "context": "Etymology, related words, cultural notes (2-3 sentences)",
  "book": "(optional) source book",
  "source": "(optional) 'generated' for Claude-suggested words"
}
```

## User Preferences
- No API key approach — user prefers pasting words in chat and getting JSON back
- Words should be uncommon, literary, evocative — the kind found in books
- Enjoys rich context: etymology, cultural significance, cross-disciplinary connections
- After pushing changes: `git push` from `C:\Users\BridgetLaroche\word-of-the-day`
