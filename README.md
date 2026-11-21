# Doodle Duel

A party drawing-and-guessing game. One screen (a laptop or TV) is the shared board, and everyone plays on their phone.

## Modes

- **Robot draws:** the robot sketches a picture in 4 seconds and everyone races to guess it within 14 seconds. The sketches come from Google's [Quick, Draw!](https://quickdraw.withgoogle.com/data) dataset: 345 subjects with about 30 different people's drawings each (10,000+ sketches), plus 49 hand-made tricky pictures. Every sketch is randomly tilted, sometimes mirrored and drawn in a shuffled order, so you can't learn how the robot draws things.
- **You draw:** players take turns. The artist picks one of three words (from 1,700+) and draws it on their phone while everyone else guesses. Letters are revealed at steady intervals. The host picks 2 to 5 rounds and 60 to 120 seconds per drawing. Drawing tools: pen, eraser, bucket fill, line, rectangle, circle (outlined or filled), 14 colours plus a full colour picker, 4 pen sizes, undo and clear.

## Scoring

- A correct guess scores between 50 and 300 points depending on how much time is left, plus a bonus of 50 for the first player to get it and 25 for the second.
- In "You draw", the artist gets 50 points for every player who guesses their drawing.
- If nobody guesses, nobody scores. A round ends as soon as everyone has guessed.
- A near miss shows "is close!" only to the player who typed it.

## How to play

1. Open the game on the shared screen. It shows a QR code and the game settings.
2. Everyone scans the QR code with their phone. People can also join mid-game from the small QR code beside the scoreboard.
3. Pick the mode and settings, then press **Start game**.

The shared screen doesn't play unless you tick "This screen plays too" (handy if only two of you are playing on two phones). Keep the shared screen awake during the game: it runs the rounds and checks the guesses.

## How it works

`index.html` holds the whole game and `drawings.json` holds the robot's sketches. Both are hosted on GitHub Pages. Phones talk through a [Supabase Realtime](https://supabase.com/docs/guides/realtime) channel, so it works on mobile data and any Wi-Fi. If a phone drops out for a moment it rejoins with its score and the current drawing.

Add `?sheet` to the address to see the hand-made pictures and a sample of the real sketches.

Sketch data: Quick, Draw! dataset by Google, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The drawings were re-encoded into a smaller format for this game.
