---
title: "Why Rejected Hypotheses Are More Valuable Than Confirmed Ones"
datePublished: 2026-05-09T16:27:11.373Z
cuid: cmoyk4cjw01jx2em7aprh7w79
slug: why-rejected-hypotheses-are-more-valuable-than-confirmed-ones
tags: analytics, product

---

*On building analysis around falsifiable hypotheses — and what you learn when the data proves you wrong.*

* * *

There is a habit in data analysis that looks like rigor but is actually its opposite.

You look at a dataset. You form an intuition about what's probably true. You build a query that confirms it. You write it up. The analysis "worked."

The problem is that you never tested anything. You found what you were looking for because you only looked where you expected to find it. The uncomfortable alternative — that your intuition was wrong — never got a real chance to surface.

This is confirmation bias dressed up as analysis. And it produces findings that feel true, read well, and guide decisions in the wrong direction.

* * *

## The alternative: build to be proven wrong

A few months ago, I ran a retention analysis on an online retail platform. Before writing a single query, I wrote seven specific, falsifiable predictions — each with a defined confirmation condition and a defined rejection condition.

I was genuinely convinced most of them were right.

Five were rejected.

Here's what those five rejections looked like:

| Hypothesis | My Prediction | What the Data Showed | Status |
| --- | --- | --- | --- |
| H1: Most customers don't return | Low repeat rate — retention problem | 72.4% repeat buyers — 3× industry benchmark | ❌ Rejected |
| H2: Returners come back quickly | Under 30 days | Median 55 days — bimodal pattern, two segments | ❌ Rejected |
| H5: Second purchase drives loyalty sharply | 2× drop-off ratio at purchase 2 | Ratio of 1.24× — loyalty builds gradually | ❌ Rejected |
| H6: Returns correlate with lower retention | More returns = more churn | More returns = higher retention (96.1% for 4+ returns) | ❌ Rejected |
| H7: Retention varies significantly by country | 20pp+ range across countries | Only 3 countries had enough volume; 7.6pp range | ❌ Rejected |

And the two I got right:

| Hypothesis | Status |
| --- | --- |
| H3: Largest drop-off after first purchase | ✅ Confirmed |
| H4: One-time and repeat buyers behave differently in session one | ✅ Confirmed |

I'll be honest — when H1 came back rejected, I sat with the result for a few minutes hoping I'd written the query wrong. I had been so certain the business had a retention problem. Finding out it didn't felt like losing the point of the whole exercise. It took a moment to realize: this is better. A business that thinks it has a retention problem and doesn't is about to waste serious money. Finding that out early is the entire value of the analysis.

* * *

## What the rejections actually taught me

**H1** told me the 72.4% repeat rate was driven by wholesale buyers and resellers — not casual consumers. The business didn't have a retention problem. It had a wrong-fit acquisition problem. That's a completely different solution.

**H6** was the most counterintuitive. Customers with the most returns retained at 96.1%. Once I stopped expecting the opposite, the reason became clear: these were resellers returning unsold inventory as part of their normal cycle. Returns were a loyalty signal. Treating them as a churn risk would have been a costly mistake.

**H5** killed a popular playbook. "Get them to buy twice and they're yours forever" is conventional retention wisdom. This dataset said no — loyalty here built gradually across every purchase, not sharply at purchase two. The recommendation changed entirely because of that rejection.

In each case, the rejection didn't just say "you were wrong." It said *here is something about how this business actually works that your intuition missed.* That's more valuable than three confirmations.

* * *

## Why most analysts skip this

Writing hypotheses before you analyze feels slower. It introduces friction. And it creates a record of being wrong.

That last part is the real reason. In professional settings, being wrong feels like weakness. The safer framing is "I explored the data and found these interesting patterns" — no predictions, no accountability, no record of what you expected.

But that safety is the problem. Exploration without prediction is documentation. You're describing what happened, not testing whether your model of the world is accurate.

* * *

## The format that makes it work

The hypothesis format I use before opening any query editor:

> **Hypothesis:** Specific, falsifiable prediction **Confirmation condition:** What the data needs to show **Rejection condition:** What the data needs to show instead **Business implication if confirmed:** What follows **Business implication if rejected:** What follows instead

That last line is the one most people skip. If you can't say what you'd recommend when wrong, you haven't thought through the problem deeply enough.

* * *

## Why this changes the output

The deliverable changes when hypotheses are defined upfront.

Instead of "here are the interesting patterns I found," the output becomes "here are the questions I asked, here is what the data said, and here is what that means for the business."

That structure is more defensible. It separates what the analyst expected from what the data showed — the most important distinction in any analytical document.

In this case, the five rejections shifted the entire recommendation. Not toward retention spending — toward acquisition strategy. The business didn't need to keep customers better. It needed to attract more of the right ones from the start.

Five of my seven hypotheses were wrong. The analysis became stronger because of it. And the resulting recommendations shifted acquisition strategy, not retention spending — which is what happens when you let the data answer honestly instead of confirming what you already believed.

* * *

**Full methodology, hypothesis framework, and code →** [**GitHub**](https://github.com/JoshuaPaul-lasisi/product-analytics-user-retention)

*The retention analysis referenced here was conducted on the Online Retail II dataset (UCI Machine Learning Repository) using Python, pandas, and matplotlib.*