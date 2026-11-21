# Doodle Duel

A party guessing game for two or more phones, with two modes:

- **Robot draws:** the robot scribbles 20 tough pictures (a stegosaurus, a seahorse, a steam train, an anglerfish…) in 4 seconds each. Every picture is tilted, sometimes mirrored, drawn in a random order and missing about a third of its lines. You have 14 seconds to guess.
- **You draw:** players take turns. The artist picks one of three words and draws it with their finger while everyone else guesses, live. You get 80 seconds, and a letter is revealed at the halfway and three-quarter marks. With up to 3 players everyone draws twice; with 4 or more, once each.

## Scoring

- The first correct guess scores 3 points, the second 2, and everyone after that 1.
- In "You draw", the artist also gets 1 point for every player who guesses their drawing.
- If nobody guesses in time, nobody scores.
- A round ends as soon as everyone has guessed. A near-miss shows "So close!" to the person who typed it, and is hidden from everyone else.

## How to play

1. Open the game on one phone. That phone is the host: it picks the mode and has the Start button.
2. Everyone else scans the QR code on the host's screen (or opens the link the host sends). Any number of players can join, even mid-game.
3. The host taps **Start game**.

Keep the host's screen on during the game: the host phone runs the rounds and checks the guesses.

## How it works

It is a single `index.html` hosted on GitHub Pages. The phones send messages through a [Supabase Realtime](https://supabase.com/docs/guides/realtime) channel, so it works on mobile data and any Wi-Fi. If a phone drops out for a moment (screen locked, signal blip), it picks the game back up with its score, and the current drawing, when it reconnects.

To check or edit the robot's drawings, add `?sheet` to the address to see all 49 pictures at once (the dashed pink lines are the ones left out during play).
