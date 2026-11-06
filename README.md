# KuroFlipper

A dependency-free Albion Online Black Market scanner that runs in your browser and fetches prices from the [Albion Online Data Project](https://www.albion-online-data.com/).

## Run it

Open `index.html` in a modern browser. No install, account, API key, or backend is required. Internet access is needed to retrieve market prices and item icons. If your browser blocks requests from local files, serve this folder with any local static web server.

## Use it

1. Select your game server, the city to buy from, the market to sell to, and item quality (Normal through Masterpiece). **All cities** compares available city markets; selling to **Black Market** remains the default.
2. Set the item tier (T1–T8) and enchantment (base or .1–.4), then click icons in the searchable item gallery to select items. The gallery loads Black Market equipment and tools from the full community-maintained Albion Online item dump; non-eligible item types are excluded. Use search or **Show more** to browse the list.
3. Choose whether your character has Premium; the sell tax estimate updates automatically (4% with Premium, 8% without). Add any extra per-item cost, such as transport.
4. The **2 best per city → Black Market** opportunities load automatically, remain visible while refreshing, and refresh the full item list every minute. The latest successful results are saved in this browser and shown while fresh prices load. Changing tier, enchantment, quality, server, or cost triggers a quicker refresh. Use **Pause live updates** to stop automatic refreshes or **Start live updates** to resume. Select **Scan market prices** to manually scan your chosen items and markets.

The market API does not provide your account's Premium status, so select it yourself; KuroFlipper applies the corresponding estimated sell tax. The estimate compares city sell listings with Black Market buy orders, showing the two highest-profit items per city, and subtracts sell tax and extra cost. Live opportunities re-query all eligible catalog items once per minute while the page is open. The Albion Online Data Project can only report prices recently observed by its community client; timestamps show when those orders were last reported, not a guaranteed real-time quote. Background tabs may be throttled by the browser. The scanner does not account for order fill probability, market listing fees, focus, or other player-specific modifiers. Verify prices in-game before trading.

If a manual scan says no matching prices were reported, the API connection succeeded but has no prices for that exact item, quality, and market combination. Try another filter or use **2 best per city → Black Market** to search the current catalog for available profitable prices.

Server, quality, city, Premium status, selected items, tier, and extra cost are saved in your browser's local storage. Market prices come from the Albion Online Data Project, item names from the community-maintained [Albion item dump](https://github.com/ao-data/ao-bin-dumps), and item pictures from Albion's community item-rendering service. The site does not have its own backend.
