# future-price-insights


	Large liquid markets are currently our best method of predicting what the price of something will be in the future. If you disagree, you're welcome to try your hand at making better predictions, and will make a lot more on that than this project could ever bring in, or more likely, lose money. 
	But that expected future price information is almost never converted into useful insights for policymakers. Neither is it packaged in a way that the public can understand. It's kept away in finance firms in Chicago and New York and London and Hong Kong.
	What kind of information do people want?
		- Combine bond prices with inflation expectations to tell me about the likelihood of repayment of government bonds. That lets me track the status of the war in Ukraine at a high level very easily, understand how well Milei is doing, or track the misadventures of Liz Truss. 
		- I heard something about a famine: another user made a bundle of staple foodstuffs and shared it to me as a list of items to track that I can past in, so I use that and see what the expected prices are in six months.
		- I need to get elected, and Americans are convinced that the president controls gas prices and vote downballot to punish or reward them. What are prices expected to be at election time?
		- Event study
			- Did policy X have an impact on price Y? What about the overall trend during the X presidency?
	How do you get it to them?
		- Providers like Bloomberg and Barchart have raw commodities futures data: you'll need to spend a little time comparing options and picking the best API, and doing some testing to make sure that the data is sensible.
		- Then you need to convert the raw data on futures and prices into meaningful information. There are plenty of textbooks and papers on options pricing at this point, and I'm happy to consult on what information is particularly policy-relevant: if you offer people data and say you want to shape it better to their wishes, many people are willing to spare an hour of advice.
		- Then you need to present that information usefully: graphs, charts, Wolfram Alpha style queries (that last one is probably not worth the effort).
	    - General point: real % change relative to today is much more important than $/barrel or $/bushel 
	- Additional bonus features, perhaps offered to patrons / paying users: auto-alerts when some values exceed a set range, weekly/daily customized newsletter with their key charts, prioritization of new info sources requests.
	What does an MVP look like?
		- Oil prices / futures, displayed a few different ways and shown over various time horizons. Other commodities are also important, but oil is highly fungible and incredibly important.
	How do they find out about it?
		- Post this to Hacker News and the rest should take care of itself.
	Why do this?
		- Policymakers would make better decisions and be more informed if they had access to high-quality information about future prices in food, oil, and other goods. They don't: it's slow and filtered by people they don't trust. 
		- Doing this well shows that you can do an independent project, handle UI, handle web development, and deliver useful information to decision makers. After successfully completing such a project, you could easily end up with a role in data engineering, or an even higher-paying role in finance.
	**Progress so far:** Preliminary survey of related existing work & of target audience’s interest
	**Source of Idea:**
		I work in tech and policy and have personally been quite frustrated by the lack of such information. I previously also wrote about this idea [here](https://arc.net/l/quote/hsvvqzbs). 
		Any decent trader can tell you that the spot price of oil futures three months out is not the same as the expected price of oil in three months, but none of them have been able to get me "what will oil prices be in three months".

[Keller Scholl Free Ideas](https://www.kellerscholl.com/free-ideas)
	- As a policy person, I would like to gain information from markets. I think many people would like this! Give me projected volatility at various time ranges and current indicators (optionally by sector), let me pick countries of interest, show it all on a dashboard, and let me set alerts (if you want to monetize it, say that email alerts cost extra, charge more for real-time, once you're providing substantial amounts of value money is easy). I think that the reason this hasn't been done yet is that anyone who can do it usefully can make a lot more money working in finance. It's a useful project that would benefit the world, and something that I think an MVP of is achievable in a college student's summer that unexpectedly freed up. I'm happy to talk through what I need and what data sources I think would be relevant, though I don't have the coding ability to supervise as the senior dev. This project requires, and gives ample opportunity to grow, really good UI skills. You're trying to make complex data presentation user-customizable. But you can start with something pretty simple. There will also be a lot of work ingesting data from other people's APIs, which is generally good practice.
    - Related point: someone with a better handle on financial mathematics than I have and more access to data could probably use futures markets to give me "current market expected price for commodity X over the next two years", as a graph. I'd love to have that for oil, a few food commodities, and perhaps automatically flagging anything with particularly sharp increases or decreases. If you want to get really fancy, let me see how this has changed over time. 1. Users should be able to find/create particular charts, adjusting time frames, putting layering items, etc.
2. There are three basic use-cases that I envision for personal use, and I'm not very confident which ones will end up being most popular or useful. 
A. A chart that answers a specific question I have, particularly about historical data. Here I'm particularly interested in plotting specific events and trying to see if the market responded in some significant way. Basically an event study analysis.
B. A chart that I want to monitor on a regular (daily/weekly/monthly/quarterly) basis, because it's important to what I do.
C. A chart that I want to ring an alarm bell whenever something "extreme", broadly defined, happens.
3. Of course, I'm also going to want to export said charts: a simple screenshot or PNG technically works, but for growth you'll be happier if users can easily share a link that allows someone to manipulate that chart as they will. 

Data: Government bond prices, with as many adjustments as possible to turn them into "percentage of debt that the government will repay, in expectation" (since you need to incorporate both haircuts and defaults). In cases of countries that issue bonds in their own currency, finding a different inflation forecast to subtract would be helpful. Commodity price forecasting (particularly for sensitive commodities like a calorie-weighted basket of foodstuffs, oil, and rare-earth minerals).



## Collaborate with GPT Engineer

This is a [gptengineer.app](https://gptengineer.app)-synced repository 🌟🤖

Changes made via gptengineer.app will be committed to this repo.

If you clone this repo and push changes, you will have them reflected in the GPT Engineer UI.

## Tech stack

This project is built with .

- Vite
- React
- shadcn-ui
- Tailwind CSS

## Setup

```sh
git clone https://github.com/GPT-Engineer-App/future-price-insights.git
cd future-price-insights
npm i
```

```sh
npm run dev
```

This will run a dev server with auto reloading and an instant preview.

## Requirements

- Node.js & npm - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
