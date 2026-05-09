---
title: "Analyzing 900K Google Analytics Sessions: Why Most Visitors Never Reached a Product Page"
datePublished: 2026-05-09T18:34:45.092Z
cuid: cmoyooe7501px2em75nwa5wl5
slug: analyzing-900k-google-analytics-sessions-why-most-visitors-never-reached-a-product-page
tags: product, business-analytics

---

Using BigQuery funnel analysis to diagnose where engagement collapsed in the Google Merchandise Store dataset.

* * *

Most e-commerce funnel discussions focus heavily on checkout optimization.

Cart abandonment. Payment friction. Shipping complexity. Account creation requirements.

These are legitimate concerns, and businesses often invest heavily in solving them.

But while analyzing roughly 903,000 Google Analytics sessions from the Google Merchandise Store dataset in BigQuery, I found that the largest conversion issue appeared much earlier in the user journey.

Long before checkout.

Long before cart interaction.

The majority of users never meaningfully engaged with a product page at all.

* * *

Dataset and approach

This analysis used the publicly available Google Analytics sample dataset in BigQuery:

~903K sessions

One full year of session-level data

Funnel built from behavioral events:

product view

add-to-cart

checkout

transaction completion

The objective was straightforward:

Build the complete acquisition funnel and identify where the largest drop-off occurred.

* * *

Funnel results

The funnel output looked like this:

Step Sessions % of Previous Step

All sessions 903,653 100% Viewed a product 123,692 14% Added to cart 50,022 40% Entered checkout 22,371 45% Completed purchase 11,552 52%

The largest drop-off occurred immediately after landing.

Only 14% of sessions resulted in a product view.

That means approximately 86% of visitors exited the site before meaningfully interacting with a product page.

By comparison, the lower funnel performed relatively normally:

40% product-view-to-cart conversion

45% cart-to-checkout progression

52% checkout-to-purchase completion

This suggested that checkout itself was not the primary issue.

The largest engagement failure occurred earlier in the funnel.

* * *

Initial hypothesis: low-quality traffic

My first assumption was that the issue originated from acquisition quality.

The reasoning seemed reasonable:

wrong audience targeting

low-intent traffic

weak acquisition channels

To test this, I segmented sessions across multiple dimensions:

traffic source

device category

country

channel grouping

I also filtered out low-volume segments to reduce small-sample distortion.

The expectation was that certain segments would show significantly stronger product-view rates.

That did not happen.

* * *

Segmentation findings

The same pattern repeated consistently across nearly every segmentation layer.

Desktop, mobile, and tablet traffic all showed similarly weak product-view behavior.

Countries with sufficient traffic volume also demonstrated low engagement rates.

Traffic-source segmentation revealed variation in scale, but not enough variation in product engagement quality to explain the funnel collapse.

In other words:

The issue was not isolated to a single acquisition channel, geography, or device type.

That consistency became important analytically.

When a behavioral problem persists across nearly every measurable segment, the explanation is less likely to be channel-specific and more likely to be systemic.

* * *

Interpreting the behavior

The Google Merchandise Store sells officially branded Google merchandise:

hoodies

bottles

caps

notebooks

stickers

The products are functional and the brand itself is globally recognizable.

However, recognition alone does not necessarily create strong exploratory intent.

Many users likely arrived through indirect exposure:

blogs

YouTube

search traffic

developer curiosity

social media referrals

But the behavioral data suggested that most users did not arrive with strong purchase intent toward Google-branded merchandise specifically.

That distinction matters.

Because users who arrive with weak product intent often exhibit shallow browsing behavior:

short sessions

minimal exploration

early exits

The funnel data reflected exactly that pattern.

* * *

Practical business implications

This changes how the business should think about optimization priorities.

A common response to weak conversion metrics is:

> “Drive more traffic.”

But if most users disengage before reaching a product page, increasing acquisition volume may simply increase disengaged traffic volume.

The more useful intervention is identifying why exploratory engagement is failing upstream.

Several areas would be worth testing:

1.  Product discovery improvements
    

clearer category visibility

stronger homepage routing

more prominent featured products

improved above-the-fold calls-to-action

2.  Product presentation
    

stronger product imagery

more aspirational merchandising

clearer lifestyle positioning

3.  Traffic-source auditing
    

Some high-volume channels demonstrated weak engagement quality and may require:

targeting refinement

creative adjustments

budget reallocation

* * *

Key analytical takeaway

The most important lesson from this project was methodological.

Without building the full funnel, it would have been easy to misdiagnose the business problem as:

checkout friction

payment abandonment

cart optimization failure

But the data showed the largest behavioral collapse occurring much earlier.

Before users even meaningfully encountered the products.

That distinction matters because optimization efforts are only effective when applied to the actual point of failure.

And in this case, the largest leak in the funnel was not checkout.

It was pre-product engagement.

* * *

This analysis was conducted using Google BigQuery on the Google Analytics sample dataset. Full SQL queries, funnel logic, segmentation methodology, and findings are available on [<mark class="bg-yellow-200 dark:bg-yellow-500/30">Github</mark>](https://github.com/JoshuaPaul-lasisi/funnel-activation).