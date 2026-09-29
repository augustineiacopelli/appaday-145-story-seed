# 145 Story Seed

**AppADay #145** | Creative | AI-powered

**Live app:** https://augustineiacopelli.github.io/appaday-145-story-seed/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

Pick a genre and name a single object, and Claude plants a two paragraph story opener in which that object is the catalyst that sets everything in motion. Tap Random for an evocative object, Regenerate for a fresh take on the same seed, and Copy to take the opener with you. Your last ten seeds stay close at hand.

## How it works

Open Settings with the gear and add your Anthropic API key and an optional session name. Both stay in your browser's localStorage and the key is sent only to api.anthropic.com. The session name signs each seed you plant.

Tap one of twelve genre chips or type your own genre, then type an object or tap Random to draw from a list of thirty six. Press Plant the seed. The app makes one call to the Messages API with `claude-sonnet-5-5`, thinking disabled, and a 600 token ceiling. The prompt asks for exactly two paragraphs of roughly 180 to 260 words that open in scene, make the object the catalyst rather than decoration, and end on a turn that pulls the reader forward. The reply is normalized into two paragraphs, stripping any stray heading, merging extras, or splitting a single block at its sentence midpoint.

## The reading card

The opener appears on a paper card with the genre and seed above it, a drop cap on the first paragraph, and the first mention of the object softly highlighted. Regenerate replants the same genre and object. Copy puts both paragraphs plus a genre and seed line on the clipboard, with a fallback for browsers without the Clipboard API.

## History

Every successful seed is saved to localStorage, newest first, capped at ten. Tap any entry to reopen it on the card, or clear the list with a two tap confirm. The most recent seed reopens automatically on your next visit.

## Tech

A single self-contained `index.html` of vanilla HTML, CSS, and JavaScript with no build step and no external assets; type uses system serif, sans, and mono stacks. The API is called directly from the browser with the `anthropic-dangerous-direct-browser-access` header and the user's own key.

---

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), one complete app shipped every day.
