# BOLTZ!

*The Shipyard Rescue.* An original retro arcade climber. Boltz the robot has nabbed Sparky the dog.
Climb the shipyard gantry, jump over oil drums, dodge sparks and crates, ride the lifts,
and pull every bolt to bring Boltz crashing down.

The whole game is one file, `index.html`. It needs no installs and no build step, and it
works on desktop and mobile.

## Play it on your computer

Double-click `index.html` and it opens in your browser.

**Desktop controls**

| Key | Action |
| --- | --- |
| ← → (or A / D) | Move |
| ↑ ↓ (or W / S) | Climb ladders |
| Space (or Z / X) | Jump |
| Enter | Start / pause |
| P | Pause |
| M | Sound on/off |

**Phone controls:** an on-screen D-pad (left), a JUMP button (right), and START / SOUND
buttons in the middle. Turn the phone sideways for a wider layout.

## Play it on your phone (GitHub Pages, free)

1. Sign in at https://github.com and create a new **public** repository, for example `boltz`.
2. In the repo, click **Add file → Upload files**, drag in `index.html`, and click **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source** to *Deploy from a branch*,
   pick the **main** branch and **/ (root)** folder, then click **Save**.
4. After a minute or two the page shows your link, like `https://<your-username>.github.io/boltz/`.
5. Open that link on your phone. To install it like an app:
   - **iPhone (Safari):** Share → *Add to Home Screen*
   - **Android (Chrome):** ⋮ menu → *Add to Home screen*

To play on your phone without GitHub, put the phone and computer on the same Wi-Fi, run
`npx http-server -p 8080` in this folder, and open `http://<your-computer's-IP>:8080` on the phone.

## How the game works

Each level is a run of stages, and every stage adds a twist:

| Level | Stages |
| --- | --- |
| 1 | Ramps → Bolts |
| 2 | Ramps → Lifts → Bolts |
| 3 | Ramps → Belts → Lifts → Bolts |
| 4+ | Ramps → Belts → Ramps → Lifts → Bolts (faster each level) |

- **The Ramps:** Boltz rolls oil drums down sloped girders. Drums sometimes drop down ladders.
  Drums that reach the furnace at the bottom turn into sparks that chase you.
- **The Belts:** conveyor belts push you around and carry crates. The middle belt flips direction.
- **The Lifts:** ride the up and down lifts. Don't ride the up-lift into the motor at the top,
  and watch for the bouncing nuts Boltz throws.
- **The Bolts:** walk over all 8 yellow bolts to pull them out. Each one leaves a gap behind you,
  so jump back over it. Pull them all and Boltz falls.

**Scoring:** jump a drum, crate or nut for 100. Smash a drum or crate with a mallet for 300,
or a spark for 500. Each bolt is 100. Whatever is left of the bonus timer is added when you
clear a stage. You get one extra life at 10,000 points.

**Rules of thumb:** a fall from more than a short hop is fatal. While you hold a mallet you
can't climb or jump. If the bonus timer reaches zero you lose a life. Your high score is saved
in the browser.

The pixel font loads from Google Fonts when you're online. Offline, the game falls back to
a built-in monospace font and still works.
