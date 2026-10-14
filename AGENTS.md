# Grandma's House — Agent Instructions

## Mission
Develop an original, browser-based, NES-inspired game platform. Preserve the approved **Style B**: warm sunset, side-on 8-bit Grandma's living room, chunky sprites, low-resolution pixel art, CRT and cartridge shelf. Avoid modern gradients, high-detail pixel illustrations and unnecessary features.

## Canonical interaction loop
1. Player enters the living room and can walk immediately.
2. At the TV with no selected cartridge, show "NO GAME INSERTED — CHECK THE BOOKSHELF."
3. Player walks to the bookshelf and chooses a cartridge.
4. A confirmation shows the selected game.
5. Player walks BACK to the television and presses interact.
6. TV offers START/CANCEL; start loads the game.
7. After playing, return to the living room with previous selection intact.

No global menu may bypass this loop in the initial version. Keep the shelf and TV as distinct interactive objects.

## First cartridge
COASTLINE '89: original California-sports-inspired collection. First playable event is HALFPIPE. Make controls simple, responsive, and intentionally classic; prioritize movement, acceleration, airborne rotation, landing and funny wipeouts. Do not reproduce original copyrighted assets, code, music or branding.

## Engineering
- Treat the initial HTML prototype as a behavior reference; preserve working interactions during refactors.
- Prefer TypeScript, Phaser, and Vite if/when a refactor materially helps; don't rewrite for its own sake.
- Render low-res game assets with nearest-neighbor scaling and a 4:3 gameplay viewport.
- Support keyboard first, then controllers, with reliable input focus and pause/resume.
- Add repeatable tests for state transitions and gameplay logic. Run tests before requesting review.
- Avoid unnecessary dependencies, paid services, accounts, tracking or analytics.

## Working protocol
- Take one scoped issue at a time, create a feature branch and small pull request.
- Every PR includes before/after behavior, tested flows, screenshots or recordings where useful, known issues, and follow-up suggestions.
- Do not merge to main, alter visual direction, add games, publish production or incur expense without the owner's approval.
- Preserve player privacy; prefer local high scores for MVP.
- An exploratory agent may recommend backlog items, but should not silently expand scope.

## Definition of done
The TV → shelf → TV loop works by keyboard; games launch and return reliably; no regressions to room navigation; input instructions visible; changes reviewable in a PR.
