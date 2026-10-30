# Feeless Stack

A free, single-file browser stacking game. Drop the sliding block, land perfect hits to keep your tower wide, and see how high you can go. No build step, no backend, no fees.

## Play

- **Drop:** tap, click or press Space to drop the sliding block. Anything that overhangs is cut off. Miss completely and the tower falls.
- **Perfect drops:** land within a few pixels of the block below and it snaps into place with nothing cut. Three perfects in a row start growing your block back, up to its starting width.
- **Coins theme (default):** every block is a coin with its ticker and colour (XNO, BTC, ETH, LTC, XMR, SOL, ADA, DOGE, XRP, BNB, DOT, TRX, repeating). Other themes are plain colours.
- **Ranks:** Paper Hands, Hodler (10 layers), Diamond Hands (20), Whale (30), Satoshi (45), with pop-ups as you climb.
- **Feedback:** a ring flash on perfect drops and a short vibration on phones that support it.
- **Bonus growth:** every 5th layer the block grows back by about 2% of the starting width, up to the starting width, whether or not the drop was perfect.
- **Speed:** blocks slide faster as the tower grows.
- **Daily challenge:** the same speeds for everyone, new every day at 00:00 UTC. Reach 30 layers to clear it and keep your daily streak.
- **Free play:** your best tower is stored per device.

Everything is stored in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `feeless-stack`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/feeless-stack/`.

## Donations

The tip card works the same way as in the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter block themes (Gold, Neon, Mint) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control.

Add `?selftest` to the URL to expose a small `window.__bs` object for automated tests.
