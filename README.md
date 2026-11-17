# Doodle Duel

A two-phone guessing game. The robot draws 20 pictures, one stroke at a time, and the first player to type what it is gets the point. Most points wins.

## How to play

1. Open the game on the first phone. That phone is the host and has the Start button.
2. The second player scans the QR code on the host's screen (or opens the link the host sends).
3. The host taps **Start game**.
4. Each picture is drawn over about 16 seconds. Type your guess and press Guess. The first correct guess wins the picture.

## How it works

It is a single `index.html` with no server of its own. The two phones talk to each other directly over WebRTC using [PeerJS](https://peerjs.com/), so both phones need an internet connection.
