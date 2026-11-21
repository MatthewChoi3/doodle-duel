# Doodle Duel

A two-phone guessing game. The robot draws 20 pictures, one stroke at a time, and the first player to type what it is gets the point. Most points wins.

## How to play

1. Open the game on the first phone. That phone is the host and has the Start button.
2. The second player scans the QR code on the host's screen (or opens the link the host sends).
3. The host taps **Start game**.
4. Each picture is drawn over about 16 seconds. Type your guess and press Guess. The first correct guess wins the picture.

## How it works

It is a single `index.html` hosted on GitHub Pages. The two phones send messages to each other through a [Supabase Realtime](https://supabase.com/docs/guides/realtime) channel, so it works on mobile data and any Wi-Fi. Both phones need an internet connection. If a phone drops out for a moment (screen locked, signal blip), it picks the game back up when it reconnects.
