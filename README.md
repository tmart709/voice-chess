# Voice Chess

Play chess against the computer by talking. Say your move, and it says its move back.
After one tap to turn on the microphone, you never need to touch the phone.

## Put it online (about 5 minutes)

The microphone only works on a secure (https) website, so the game has to be hosted.
GitHub Pages does this for free, the same way as the Market Monitor.

1. Sign in at https://github.com and click **+** (top right) → **New repository**.
   - Name: `voice-chess`
   - Visibility: **Public**
   - Click **Create repository**.
2. Click **uploading an existing file**. Drag in **everything inside** the `voice-chess` folder
   (`index.html`, `manifest.webmanifest`, `icon.svg`, `icon-180.png`, `icon-192.png`, `icon-512.png`),
   then click **Commit changes**.
3. Go to **Settings → Pages**. Under **Source**, choose **Deploy from a branch**.
   Pick branch **main**, folder **/ (root)**, and click **Save**.
4. After about a minute, your game is live at:
   `https://YOUR-USERNAME.github.io/voice-chess/`

## Put it on your phone

Open the link on your phone, then:
- **iPhone (Safari):** Share button → **Add to Home Screen**
- **Android (Chrome):** ⋮ menu → **Add to Home screen**

Tap **Start listening** and allow the microphone when asked.

If voice doesn't work from the home-screen icon on iPhone, open the link in Safari instead.
Some iOS versions limit speech recognition in home-screen apps.

## Things you can say

| Say | What it does |
|---|---|
| "e4", "pawn to e4" | Move a pawn |
| "knight f3", "knight to f3" | Move a piece |
| "bishop takes c6", "e takes d5" | Capture |
| "castle kingside", "short castle", "long castle" | Castle |
| "e8 queen" | Promote (queen if you don't say) |
| "knight from g1 to f3" | Pick which piece when two could move there |
| "undo" | Take back your last move |
| "repeat" | Hear the computer's last move again |
| "hint" | Get a suggested move |
| "read the board" | Hear where every piece is |
| "blindfold" / "show board" | Hide or show the pieces |
| "Elo 1500", "fifteen hundred rating", "easier", "harder" | Set your opponent's rating (400 to 3000) |
| "new game", "play black", "play white" | Start over |
| "flip board" | Turn the board around |
| "pause" / "resume" | Stop reacting until you say "resume" |
| "resign" | Give up |

If two pieces can reach the square you said, it asks "Which knight?". Answer with the square, like "b1".
You can also tap pieces to move them.

## Good to know

- The computer opponent is Stockfish, a free open-source chess engine. It loads from the internet.
  If it can't load, a simpler built-in opponent plays instead, and the top right says "lite engine".
  The backup opponent plays at about 1400 at most, whatever rating you pick.
- Opponent ratings are approximate. You can also pick one from the "vs Elo" menu at the top.
  Each rating sets Stockfish's skill level and how deeply it searches. Ratings of 1400 and below
  also make it play an occasional random move, the way beginners blunder.
- The screen stays on while the game is open, so the microphone keeps listening.
- Speech recognition on iPhone and Android uses Apple's or Google's speech service, so you need an internet connection.
- Phones stop the microphone when the app goes to the background. Come back to the app and it starts listening again.
