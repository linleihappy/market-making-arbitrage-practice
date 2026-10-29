# The Quote Room — Market Practice

A single-page practice game for spotting arbitrage in randomized synthetic markets and checking trades against displayed prices and volume. It uses simulated quotes only; it does not place real trades.

Copyright © 2026 [linleihappy](https://github.com/linleihappy).

## Run the game

1. Download or clone this repository.
2. Open `index.html` in a modern browser. An internet connection is needed to load the hosted fonts and PeerJS library.

For a shareable browser link, enable GitHub Pages in **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, then save. Open the URL GitHub provides. Making the repository public by itself does not create a hosted website.

## Practice a market

1. Read the combo equation and the bid, offer, and displayed size for every instrument.
2. In **Scan the market**, choose whether a tradeable arbitrage exists. Compare executable synthetic prices and available depth, and use any known payout bounds shown in the market description.
3. If there is an arbitrage, use the deal ticket to select **Buy**, **Sell**, or no order for each instrument and enter quantities. Buys execute at the offer; sells execute at the bid. Quantities cannot exceed the corresponding offer or bid size.
4. Submit a complete hedge at the maximum executable volume, or trade only the combo when its known value bounds guarantee a profit. The ticket then reports the trade's P&L. If there is no arbitrage, step 2 is completed automatically.
5. Select **New market** for another randomized round.

Rounds combine synthetic spreads and signed or weighted multi-leg baskets (weights are at most 3) with fixed-total markets. Examples include film ratings, trading cards, city temperatures, theater estimates, commuter counts, card suits, neighborhood populations, event attendance, and survey responses. Quote prices and bid/offer sizes vary each round; population-style totals are randomized up to 500.

## Compete with friends

1. Open the same game on each device and select **Compete with friends**.
2. The host chooses **Create a room**, enters a name, and sets a whole-minute time limit from 1 to 10 minutes. Share the six-digit room code.
3. Other players choose **Join a room**, enter their names and the code, then wait in the lobby. Rooms support 2–6 players.
4. The host starts the match. Everyone plays simultaneously and progresses independently. A correct scan earns 5 points; a correct trade earns 5 more. A wrong answer or trade freezes that player for 5 seconds while the shared clock keeps running. If a market has no arbitrage, step 2 is automatically correct.
5. When time runs out, the leaderboard shows the winner. The host can choose **Play again** to restart with the same room.

Keep the host's browser tab open for the whole match. Multiplayer uses PeerJS for peer connections, so every device needs an internet connection and access to the PeerJS service.
