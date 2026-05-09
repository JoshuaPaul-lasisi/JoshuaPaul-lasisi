---
title: "What 72% Repeat Purchase Rate Taught Me About Who Not to Market To"
datePublished: 2026-05-09T15:29:41.899Z
cuid: cmoyi2ex501i02em776nr5vu5
slug: what-72-repeat-purchase-rate-taught-me-about-who-not-to-market-to
ogImage: https://cdn.hashnode.com/uploads/og-images/69ff1e8bf239332df499f12c/db79ad66-67fd-4d5a-9213-8fabe9398868.png
tags: analytics, product, retention

---

A Lagos-based analyst examines a UK retail dataset — and discovers that the business never really had a retention problem to begin with.

* * *

I tested seven hypotheses against the Online Retail II dataset (UCI ML Repository) using Python and pandas—cohort retention curves, first-session behavioral splits, and CLV segmentation.

When I began this analysis, I was searching for a retention problem.

That was the expectation.

Two years of transactional retail data. Over a million rows. Roughly 6,000 customers. Tens of thousands of invoices.

Classic e-commerce terrain.

And from experience, one expects the usual story:

Acquire customers. Convert them once. Lose most of them shortly after. Repeat the cycle.

That is the way of the world.

So naturally, I assumed the repeat purchase rate would reveal weakness.

Instead, the data contradicted me almost immediately.

* * *

What the data revealed

72.4% of customers made more than one purchase.

Now pause there.

Most e-commerce businesses celebrate when repeat purchase rates cross 30% for consumer retail.

Industry averages often sit somewhere between 20–40%.

This business was sitting at 72.4%.

Not slightly above average. Not “performing well.”

Abnormally high.

And strangely enough, the framing around the business did not reflect how unusual that number truly was.

The analysis I built to discover a retention problem had accidentally proven the opposite:

The business was already retaining people exceptionally well.

At least... a certain kind of people.

* * *

The first assumption failed again

My immediate conclusion was simple:

“Good. Retention works. Scale acquisition.”

Bring in more users. Let the retention engine handle the rest.

Reasonable logic.

But before accepting that conclusion, I needed to understand who exactly these returning customers were.

Because metrics speak.

And a number as high as 72.4% is rarely random.

So I kept digging.

53,628 invoices across 5,942 customers.

That averages roughly 9 invoices per customer over two years.

For a retail platform selling gifts, décor, and novelty items?

That is unusually high.

Then I examined returns and cancellations.

And this is where the analysis stopped behaving normally.

Customers with 4 or more returns retained at 96.1%.

Non-returners retained at 58.3%.

Read that again.

The people returning the most products were also the people staying the longest.

Completely backwards.

Or so it seemed.

And then the picture clicked.

Not mathematically.

Humanly.

* * *

What was actually happening

This was never truly a casual consumer customer base.

Not primarily.

The behavioral patterns gave them away.

Frequent purchases. Frequent returns. High invoice volume. Sustained engagement over time.

These were not ordinary shoppers buying birthday gifts and scented candles on impulse.

These were resellers.

Wholesale-oriented buyers.

Small operators running miniature businesses through the platform itself.

And suddenly everything made sense.

The returns were not signs of dissatisfaction.

They were inventory behavior.

Unsold items returned. Fast-moving products reordered. Demand tested in cycles.

The “customer” was behaving less like a shopper and more like a merchant.

That realization changed the entire meaning of the dataset.

The 72.4% repeat purchase rate was no longer merely a retention metric.

It was evidence of a business model hiding inside another business model.

* * *

The question changed

Initially, the question was:

“How do we improve retention?”

But the data forced a different question entirely:

“How do we acquire more customers who already behave like the ones that stay?”

That is a radically different problem.

Improving retention assumes the current customer base is fundamentally correct and merely needs encouragement to remain longer.

But the data suggested something else:

The loyal customers were already loyal.

The issue was not retention.

The issue was customer fit.

The 27.6% who disappeared after one purchase were not failed loyalists.

They were different people entirely.

Casual buyers. Campaign-driven traffic. One-time purchasers with no structural reason to return.

And no amount of discount emails or loyalty points can manufacture long-term intent where none existed in the first place.

* * *

The signal appeared early

This was perhaps the most interesting part of the entire analysis.

I separated customers into two groups:

One-time buyers

Repeat buyers

Then I examined only their first-session behavior.

Before retention mechanics. Before remarketing. Before loyalty campaigns.

The differences were already visible immediately.

Repeat buyers:

Spent 32% more in their first session

Purchased 26% more items

Explored 19% more product categories

The people who stayed behaved differently from day one.

Not subtly.

Structurally.

Because they were not shopping recreationally.

They were sourcing inventory.

And this means something important for businesses:

Loyalty often announces itself early.

The activation threshold exists in the data.

A customer who explores broadly, spends aggressively, and purchases with volume in session one is not merely “engaged.”

They are statistically more likely to become long-term revenue.

Which means businesses can act immediately.

Wholesale onboarding. Dedicated account management. Personalized retention sequences. Priority servicing.

The signs appear long before the second purchase occurs.

* * *

What this means beyond this dataset

This lesson extends far beyond one UK retail platform examined by a man sitting in Lagos with a notebook, SQL queries, and too many tabs open at midnight.

The deeper lesson is this:

Assumptions distort analysis.

We often decide what the problem is before the data speaks.

And once the mind accepts a narrative, it begins searching merely for confirmation.

The original assumption here was textbook e-commerce reasoning:

“Retention is weak.”

But reality proved stranger.

The business possessed an unusually loyal wholesale core hidden beneath aggregate averages.

Two customer worlds existed simultaneously:

A loyal reseller ecosystem

A casual consumer periphery with natural churn

Combined together, they produced one healthy-looking average.

But averages are diplomatic.

Segmentation tells the truth.

* * *

The uncomfortable recommendation

And now we arrive at the part most growth teams dislike hearing.

Stop trying to retain people who were never going to stay.

Not every lost customer is a failure.

Some customers are simply wrong-fit acquisitions.

The one-time buyer who arrived through a campaign, purchased impulsively, and vanished afterward is not necessarily a retention problem.

Sometimes he is merely evidence of poor targeting.

And pouring loyalty programs, re-engagement emails, discounts, and incentives into such users often becomes an expensive attempt to negotiate against reality.

The wiser path is harsher.

Let them go.

Redirect the effort toward finding more people who resemble the loyal core.

More resellers. More wholesale-minded buyers. More structurally aligned customers.

Because growth is not merely about increasing numbers.

It is about increasing the right numbers.

And the data will usually tell you who those people are...

...if you ask it honestly enough.

* * *

This analysis was conducted using the Online Retail II dataset (UCI Machine Learning Repository) with Python, pandas, and matplotlib. Full methodology, hypothesis testing process, and project code are available on [GitHub](https://github.com/JoshuaPaul-lasisi/product-analytics-user-retention).