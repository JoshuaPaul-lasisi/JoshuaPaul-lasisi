---
title: "Why 86% of Visitors Never See a Product — And Why That Matters More Than Checkout"
datePublished: 2026-05-09T12:01:24.370Z
cuid: cmoyamjrj019j2em7482103w2
slug: why-86-of-visitors-never-see-a-product-and-why-that-matters-more-than-checkout
tags: product, data-analytics

---

*A reflection on the Google Merchandise Store funnel, user intent, and the strange reality of modern e-commerce.*

* * *

When discussions on e-commerce conversion arise, men often rush toward checkout.

Cart abandonment. Payment friction. Long forms. Forced account creation before purchase. The usual suspects.

And yes, these things matter.

But upon examining a year's worth of Google Analytics data from the Google Merchandise Store — over 903,000 sessions across one full year — I found something rather unsettling:

The real problem begins long before checkout is ever reached.

In fact, long before desire is even formed.

* * *

## What the funnel revealed

Upon building the acquisition funnel, the figures appeared thus:

| Step | Sessions | % of Previous Step |
| --- | --- | --- |
| All sessions | 903,653 | 100% |
| Viewed a product | 123,692 | 14% |
| Added to cart | 50,022 | 40% |
| Entered checkout | 22,371 | 45% |
| Completed purchase | 11,552 | 52% |

Now pause at the second line.

Only 14% of all sessions resulted in a product view.

Which means that roughly 86% of visitors arrived at the store, wandered briefly, and departed without meaningfully engaging with a single product.

That is the wound.

Not checkout.

Not payment.

Not shipping.

The leakage occurs before interest is properly born.

And strangely enough, everything *after* product view appears relatively functional. Not extraordinary, but functional.

40% from product view to cart. 45% from cart to checkout. 52% from checkout to purchase.

The lower funnel survives.

The upper funnel hemorrhages.

* * *

## The first assumption failed

Naturally, my first instinct was to blame traffic quality.

Wrong audience. Weak targeting. Low-intent visitors.

Simple enough.

So I segmented the data.

275 unique traffic sources. Grouped by product-view rate. Sources under 100 sessions removed to reduce noise.

And then came the strange part:

Not one high-volume traffic source qualified as “high quality.”

None crossed a 60% product-view rate.

So I moved further.

Desktop. Mobile. Tablet.

Same pattern.

Then geography.

121 countries examined. 30 passed the minimum threshold.

Again:

No standout quality segment.

At this point, the pattern itself becomes information.

When every segmentation cut reveals the same weakness, the issue no longer belongs to the segments.

It belongs to the thing itself.

* * *

## What is actually happening here?

The Google Merchandise Store sells officially branded Google merchandise:

Hoodies. Water bottles. Journals. Caps. Stickers.

Recognizable products. Functional products. Even exclusive products.

And yet exclusivity alone does not create desire.

That is the crucial distinction.

A thing may be unique without being aspirational.

People arrive at the store through many routes:

Some are Google enthusiasts. Some arrive from YouTube or blog content. Some are developers merely curious. Some likely stumbled upon the store accidentally through campaigns or referrals.

But most arrive without a strong internal desire to own Google-branded apparel.

And therein lies the fracture.

The brand possesses technological authority, yes.

But authority in technology is not automatically authority in lifestyle identity.

Luxury brands understand this deeply.

Men do not purchase certain products merely because they function.

They purchase symbols. Associations. Statements. Identity projections.

The product becomes social language.

Google merchandise, for many visitors, has not yet become such language.

And because of this, visitors arrive... but do not linger.

* * *

## What this means for businesses

Conventionally, low conversion rates are answered with more traffic.

Run more ads. Increase impressions. Scale acquisition.

But what happens when the majority of visitors disengage before desire even begins?

More traffic merely multiplies disengagement.

One does not solve leakage by increasing water pressure into a broken pipe.

One first examines the fracture.

* * *

## Diagnosing the real issue

Now, pre-engagement dropout can emerge from several places.

### If it is a landing-page problem:

Visitors are not efficiently routed toward products.

The issue then becomes navigational.

Poor product discovery. Weak calls-to-action. Unclear hierarchy. Insufficient visual pull.

This is a UX problem.

* * *

### If it is a traffic-quality problem:

Certain channels are attracting low-intent users.

This becomes an acquisition problem.

Audit the channels. Reduce spend where engagement remains weak. Retarget differently.

In this dataset, platforms like m.facebook.com, t.co, and reddit.com showed high traffic volume with relatively weak engagement.

Reasonable candidates for scrutiny.

* * *

### But if it is a desirability problem:

Then funnel optimization becomes cosmetic.

For no amount of checkout refinement can save a product people never desired to explore in the first place.

And this, I believe, is the deeper issue revealed here.

Because the low engagement persisted across:

*   Devices
    
*   Countries
    
*   Traffic sources
    
*   User segments
    

The consistency of the weakness eliminated many alternative explanations.

The pattern pointed repeatedly toward the same conclusion:

The problem was not merely visibility.

It was pull.

* * *

## The practical lesson

Before optimizing checkout flows...

Before purchasing funnel software...

Before endlessly A/B testing button colors...

Build the full funnel first.

Observe where desire dies.

For sometimes the issue is indeed checkout.

Sometimes it is payment friction.

But other times?

86% of visitors leave before seeing a single product.

And no checkout optimization on earth will rescue users who never intended to stay.

* * *

*This analysis was conducted using Google Analytics session data queried in Google BigQuery. Full SQL methodology, funnel construction, and findings are available on* [*GitHub*](https://github.com/JoshuaPaul-lasisi/funnel-activation)*.*