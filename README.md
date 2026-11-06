# KuroFlipper

A dependency-free Albion Online Black Market scanner that runs in your browser and fetches prices from the [Albion Online Data Project](https://www.albion-online-data.com/).

## Run it

Open `index.html` in a modern browser. No install, account, API key, or backend is required. Internet access is needed to retrieve market prices and item icons. If your browser blocks requests from local files, serve this folder with any local static web server.

## Use it

1. Select your game server, the city to buy from, the market to sell to, and item quality (Normal through Masterpiece). **All cities** compares available city markets; selling to **Black Market** remains the default.
2. Set the item tier (T1–T8) and enchantment (base or .1–.4), then click icons in the searchable item gallery to select items. The gallery loads Black Market equipment and tools from the full community-maintained Albion Online item dump; non-eligible item types are excluded. Use search or **Show more** to browse the list.
3. Choose whether your character has Premium; the sell tax estimate updates automatically (4% with Premium, 8% without). Add any extra per-item cost, such as transport.
4. Select **Scan market prices** for the selected items, or use **2 best per city → Black Market** in the item picker to find up to two profitable items from each supported city, including Caerleon and Brecilien (up to 14 opportunities). This view checks prices every 10 seconds and rediscovers the full item list every minute while open. Changing a relevant filter or returning to the tab triggers a full refresh.

The market API does not provide your account's Premium status, so select it yourself; KuroFlipper applies the corresponding estimated sell tax. The estimate compares city sell listings with destination buy orders and picks the route with the highest estimated net profit for each item. It subtracts sell tax and extra cost. The per-city Black Market list requests fresh API responses every 10 seconds for its current candidates and rediscovers all matching items every minute. The Albion Online Data Project can only report prices recently observed by its community client; timestamps show when those orders were last reported, not a guaranteed live quote. It does not account for order fill probability, market listing fees, focus, or other player-specific modifiers. Verify prices in-game before trading.

Server, quality, city, Premium status, selected items, tier, and extra cost are saved in your browser's local storage. Market prices come from the Albion Online Data Project, item names from the community-maintained [Albion item dump](https://github.com/ao-data/ao-bin-dumps), and item pictures from Albion's community item-rendering service. The site does not have its own backend.
