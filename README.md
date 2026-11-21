# Doodle Duel

A party guessing game for two or more phones. The robot sketches 20 tough pictures (a stegosaurus, a seahorse, a steam train, a chess knight…) in about 6 seconds each, one stroke at a time and in a random order. The first player to type what it is gets the point. Most points wins.

## How to play

1. Open the game on one phone. That phone is the host and has the Start button.
2. Everyone else scans the QR code on the host's screen (or opens the link the host sends). Any number of players can join, even mid-game.
3. The host taps **Start game**.
4. You have 12 seconds per picture. Type your guess and press Guess. The first correct guess wins the picture.

Keep the host's screen on during the game: the host phone runs the rounds.

## How it works

It is a single `index.html` hosted on GitHub Pages. The phones send messages through a [Supabase Realtime](https://supabase.com/docs/guides/realtime) channel, so it works on mobile data and any Wi-Fi. If a phone drops out for a moment (screen locked, signal blip), it picks the game back up with its score when it reconnects.

To check or edit the drawings, add `?sheet` to the address to see all 45 pictures at once.
