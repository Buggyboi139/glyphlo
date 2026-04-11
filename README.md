# Glyphlo

## Overview
Live at https://glyphlo.com Glyphlo is a browser-based, offline-capable word puzzle game deployed as a Progressive Web App (PWA). Players untangle scrambled letters arranged in a circular node graph to synchronize the correct word sequence.

## Gameplay Mechanics
* **The Objective:** Swap the letter nodes to spell the hidden target word. 
* **The Rules:** The word must be read clockwise, always starting from the distinct starting node (highlighted with a gray gradient).
* **Controls:** Tap two nodes sequentially to swap their positions, or drag and drop one node onto another.
* **Progression:** The game features staged progression, starting at 4-letter words and scaling up to 8-letter puzzles. Players must solve a set number of stages to unlock the next difficulty tier.
* **Daily Challenge:** A timed, three-stage gauntlet (5, 6, and 7-letter words) that tracks completion time and restricts replays until the next calendar day.

## Core Features
* **Dictionary Integration:** Fetches real-time definitions for the generated target words using a public dictionary API.
* **Assistive Hint System:** Players can use a hint to automatically lock a correct letter into its proper node if they get stuck.
* **Local Persistence:** Progression, unlocked tiers, and Daily Challenge completion times are stored locally using the browser's `localStorage` API.
* **Audio Engine:** Utilizes a custom, multi-channel audio pool for background music and simultaneous sound effects, engineered to bypass mobile browser audio interaction restrictions.

## Technology Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
* **Architecture:** Progressive Web App (PWA) utilizing a Service Worker (`sw.js`) and web manifest for native-like installation and offline caching.
* **Graphics & UI:** CSS-driven animations combined with dynamic SVG rendering for the node connection wires.
* **External APIs:** Integrates `random-word-api.herokuapp.com` for dynamic word generation and `api.dictionaryapi.dev` for definitions.

## Deployment
The application is entirely client-side and requires zero build steps or server-side rendering. It can be hosted directly via any static file server or hosting platform.
