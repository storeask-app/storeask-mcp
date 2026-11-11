# StoreAsk

**Connect your WooCommerce store to your AI assistant**

StoreAsk connects your WooCommerce store to the AI assistant you already use, Claude or ChatGPT. On its own, an assistant can't see your orders, so it guesses or asks you to paste in exports. With StoreAsk it works from your real numbers, so it becomes your strategy, marketing and merchandising team in one chat.

Figure out how to:

- **Beat your best months:** find what drove them and have your assistant build the plan to beat them: which channels to double down on, which campaigns to run bigger, which products to push
- **Make more on every order:** see which products carry your profit, which sell the add-ons, and which first purchases turn into repeat customers, then get prices, bundles and offers built on how past changes played out
- **Turn one-time buyers into regulars:** find who bought once and never came back, and have your assistant write the emails that bring them back
- **Numbers you can trust:** counted the way WooCommerce Analytics counts them, with how each figure was worked out

Setup takes about a minute: approve access on WooCommerce's own screen in your WordPress admin, then paste one address into Claude or ChatGPT. No WordPress plugin to install, no code.

## What you need

- A WooCommerce store, connected to a StoreAsk account at [storeask.app](https://storeask.app).
- A StoreAsk plan: per team, by number of stores, with a 30-day money-back guarantee. See [pricing](https://storeask.app/pricing).

## Install

In Claude, add StoreAsk from the plugin directory.

In Claude Code:

```
/plugin marketplace add storeask-app/storeask-mcp
/plugin install storeask@storeask
```

The first time Claude uses StoreAsk, it asks you to sign in to your StoreAsk account and allow access.

## Ask about your store

- What drove our three best months, and how do we beat them?
- Plan our Black Friday around what worked the last three years.
- Which channels and campaigns brought in our best customers?
- Which products could take a higher price?
- What do people buy together, and what bundle should we make?
- Who used to buy every month but stopped? Write them a win-back email.
- What should we order before Christmas?
- Why were sales down last week?

## What's in this plugin

**The StoreAsk connector** (`.mcp.json`): a remote MCP server at `https://storeask.app/mcp`, with these tools.

| Tool | What it does |
| --- | --- |
| **List Stores** (`list_stores`) | The stores on your account and how up to date they are. |
| **Sales Summary** (`sales_summary`) | Your sales for a period, the same figures as in WooCommerce Analytics. |
| **Sales Breakdown** (`sales_breakdown`) | Your sales split by product, category, country, traffic source, coupon and more. |
| **Sales Timeseries** (`sales_timeseries`) | Your sales per day, week, month or year, to show a trend. |
| **Explain Change** (`explain_change`) | Why sales went up or down compared with an earlier period, and what it lined up with. |
| **Price History** (`price_history`) | What a product was priced at and actually sold for over time. |
| **Price Change Impact** (`price_change_impact`) | How a product sold before and after a price change. |
| **Profit** (`profit`) | Profit and margin on your products, for products with a known cost. |
| **Customer Insights** (`customer_insights`) | Your best customers, how many come back, and customers who stopped buying. |
| **Coupon Performance** (`coupon_performance`) | How your coupons did: orders, sales, discounts given, and new customers they brought. |
| **Inventory Status** (`inventory_status`) | Stock left, when products run out, when to reorder, and what your stock is worth. |
| **List Events** (`list_events`) | Sales, campaigns, notes and price changes in a period. |
| **Orders** (`orders`) | Individual orders and order counts by status, including failed and cancelled orders. |
| **Sales Pace** (`sales_pace`) | Whether this month, quarter or year is on track, and what you need per day to hit a target. |
| **Unsold Products** (`unsold_products`) | Products that haven't sold for a while. |
| **Bought Together** (`bought_together`) | Which products people buy together, for bundles and cross-sells. |
| **Find Products** (`find_products`) | Finds your products by name or SKU, with prices and stock. |
| **Find Categories** (`find_categories`) | Finds your product categories by name. |
| **Calculate** (`calculate`) | Does exact arithmetic on figures the other tools found, so the assistant never does sums in its head. |
| **Add Event** (`add_event`) | Saves something that happened, like a sale or a campaign, so later answers can mention it. Saved in StoreAsk only. |
| **Set Product Cost** (`set_product_cost`) | Saves what a product costs you, so profit can be worked out. Saved in StoreAsk only. |

**The `woocommerce-store-questions` skill**: tells Claude which StoreAsk tools to use for common questions (reviews, sales changes, pricing, customers, stock) and how to quote the figures they return.

## Your data

- The plugin contains a connector setting and a skill. The connector links Claude to one server, `https://storeask.app/mcp`, where you sign in with OAuth.
- When you ask a question, Claude calls StoreAsk's tools, and StoreAsk answers from the data it has imported from your store with the access you approved in your WordPress admin.
- Add Event and Set Product Cost save a note or a product cost in your StoreAsk account.
- StoreAsk doesn't store your customers' names, email addresses, phone numbers or addresses; it works with customer numbers. Customer names appear in Claude only if you turn on "Show customer names in AI chats" in StoreAsk.
- What you see in Claude is processed under your own agreement with Anthropic.

Details: [privacy policy](https://storeask.app/privacy), [terms](https://storeask.app/terms), [subprocessors](https://storeask.app/subprocessors).

## Help

Setup guide and troubleshooting: [storeask.app/docs/claude](https://storeask.app/docs/claude). All docs: [storeask.app/docs](https://storeask.app/docs). Email: support@storeask.app.

## License

The plugin's files are MIT licensed (see [LICENSE](LICENSE)). StoreAsk itself is a hosted service, covered by its [terms](https://storeask.app/terms).
