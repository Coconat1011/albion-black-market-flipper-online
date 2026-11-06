# KuroFlipper

A dependency-free Albion Online Black Market scanner that runs in your browser and fetches prices from the [Albion Online Data Project](https://www.albion-online-data.com/).

## Run it

Open `index.html` in a modern browser. No install, account, API key, or backend is required. Internet access is needed to retrieve market prices and item icons. If your browser blocks requests from local files, serve this folder with any local static web server.

## Use it

1. Select your game server, source city or all royal cities, and item quality.
2. Set the item tier and enchantment, then click icons in the searchable item gallery to select them. You can also use a quick-fill preset.
3. Choose whether your character has Premium; the sell tax estimate updates automatically (4% with Premium, 8% without). Add any extra per-item cost, such as transport.
4. Select **Scan market prices**. Results are ranked by estimated net silver profit and show the highest ROI separately.

The market API does not provide your account's Premium status, so select it yourself; KuroFlipper applies the corresponding estimated sell tax. The estimate compares the cheapest city sell listing with the highest Black Market buy order and subtracts that tax and the extra cost. It does not account for order fill probability, market listing fees, focus, or other player-specific modifiers. Treat community-reported prices as snapshots and verify them in-game before trading.

Server, quality, city, Premium status, selected items, tier, and extra cost are saved in your browser's local storage. Market prices come from the Albion Online Data Project, and item pictures load from Albion's community item-rendering service. The site does not have its own backend.
