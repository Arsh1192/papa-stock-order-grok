# PAPA STOCK — one-tap order page

A single static page used by the PAPA STOCK Grok board. After the owner approves a ticket in the MB Master chat,
MB sends a link to `order.html` with the order in the part after `#`. That part stays in the browser and is never
sent to any server. The page shows the order and hands it to Zerodha's own Kite order screen
(`https://kite.zerodha.com/connect/basket`). The owner logs in and confirms there.

- Only NSE, CNC (cash, no margin), LIMIT or SL orders. Anything else is refused.
- Links expire (20 minutes by default).
- No secrets live here. The Kite API key in a link is public by design. The API secret is never used.
