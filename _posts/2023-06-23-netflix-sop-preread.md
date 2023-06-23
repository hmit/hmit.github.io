---
layout: single
title: Netflix SOP
header:
  image: /assets/images/netflixsop.png
  caption: "Photo credit: [**Polaris**](https://polarisproject.org/blog/2018/07/netflixs-ozark-money-laundering-and-massage-parlor-trafficking/)"
---

## Intro
I work at Netflix, Inc —— the streaming company that started out as a mail-in-DVD business. It is a unique place in my opinion, with a scary looking [culture philosophy](https://jobs.netflix.com/culture) - at least from the outside. We are so proud of our culture that we even wrote a book about it [No Rules Rules](https://www.goodreads.com/en/book/show/49099937).

The part I'm focusing to choose here is the compensation philosophy —— **All Cash**  💵 💵 💵 💵 💵....

But with a twist: Stock Options. 

How they work at Netflix and how to evaluate them has been written about quite extensively on the web like [here](https://graystoneadvisor.com/blog/netflix-supplemental-stock-options), [here](https://faangpath.com/blog/netflix-stock-prices-employee-compensation/), or [here](https://blog.myrawealth.com/insights/a-guide-on-netflixs-benefits-program#:~:text=Netflix%20automatically%20provides%20free%20stock,stock%20options%20are%20NOT%20stocks).

## SOP tldr;
A good tldr is that you allocate a portion of your cash salary (pre-tax) —— SOP allocation. This is used to buy 10-year NSO stock options at 40% of the closing price (also the strike price) on the first trading day of every month. You pay closing price when you exercise the option. SOP allocations are made once per year in early December of the year prior. It makes for an interesting team lunch conversation come allocation deadline.

Now, it's quite hard to predict next year much less ten years so employees make a bet on stock going up to cash in on options leverage.
The way I think about my SOP allocation is:

1. call me stupid money —— money I'm okay losing in hope of trading riches
2. something that keeps Yashi happy in case the bet doesn't pay off

## Motivation
Quite a few of my Netflix colleagues have been similarly bullish on Netflix SOP albeit for different varied reasons. Those smart folks have created numerous calculators/spreadsheets to track SOP performance and having different cuts and visualizations of the data.

In that spirit, I too had a simple spreadsheet that showed me the current value of my SOP portfolio. More recently, I needed to add time-value concepts to it to further augment my "analysis".
I decided to do it as a web-app (local only) for others to also use at [netflix-sop-calculator]({{site.url}}/netflix-sop-calculator). Feel free to give it a try and suggest improvements!

This work is built on top of prior work by my colleagues:
1. Option tracker by Harshad Phadke
1. Black Scholes Valuation Model by Kevin Mao

Please, I'm happy to link to your preferred profiles if you ping me.

I'd also be remiss if I don't mention chat-GPT that wrote the initial webpage and came in handy numerous times to a javascript newbie like me.

## How to use calculator
1. Add your annual SOP allocation for every year (including the 5%) along with the year. This is stored in local storage.
2. Click on the year row to get monthly allocation detail.
3. For months with no SOP grant, you can delete them using the action ❌. This comes in handy for me because I started in the middle of the year. The actions are cached locally.
4. Put in your `Target Price` to calculate portfolio value, otherwise use the latest price.
5. The price data is fetched from [this spreadsheet](https://docs.google.com/spreadsheets/d/1WnQdKVUhEVPwN0b6gxOh6c6dUYbuHZCNPkDD6A4p5l0/edit#gid=0) and you might need to open it to refresh the latest data.