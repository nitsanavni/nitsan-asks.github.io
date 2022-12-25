---
layout: post
title: A Continuous Approach to Financial Independence
---

Note:

-   For the sake of fluency I'm writing this post in the form of an email to a friend
-   This is still a work in progress

I wanted to share with you something I've been contemplating that's related to **Financial Independence (FI)**. As you know, I am following this space since some years and together with Maya am practicing and living out some of the tenants.

## The Gist

At some point on the path to FI, we can start exercising the options we gained from our accumulated wealth and start gradually reducing our workload even before being completely Financially Independent. While delaying the exact point in time we reach full FI, this approach might be a better use of our time overall.

Instead of working full-time and retiring abruptly:

![](</images/W(t)%20step%20function.png>)

Consider this:

![](</images/W(t)%2050%20slope.png>)

## Mr Money Mustache's Seminal Post

My thoughts follow a seminal post by Mr Money Mustache (MMM) - [The Shockingly Simple Math Behind Early Retirement](https://www.mrmoneymustache.com/2012/01/13/the-shockingly-simple-math-behind-early-retirement/).
The shockingly simple math clarifies: Your savings-rate (`SR`) is the sole predictor of your mandatory career length (`L`). If you value FI, only spend on what's most valuable to you, and you will reach it much sooner; Years sooner.

Savings-rate can be defined by:

```
SR = (I-E)/I
```

`SR`: Savings-rate

`I`: Income

`E`: Expenses

Example:

With income `I=10`, and expenses `E=8`, `SR` can be calculated with `SR=(10-8)/10=20%`, and the mandatory career length is: `L=37` years.

Cutting down expenses to `E=7`, will result in `SR=30%`, `L=28` years. That's a 9 years shorter mandatory career, a decade.

Notice how a reduction of only 12% in `E`, results in a shortening of 24% in `L`.

More examples, of reducing `E`:

-   `E` 7->6 (-14%), `SR` 30%->40% (+33%), `L` 28->22 (-21%)
-   `E` 9->8 (-11%), `SR` 10%->20% (+100%), `L` 51->37 (-27%), that's a decade and a half less!

I recommend reading more on his blog, it's gold.

## A Working Career as a Step Function

One thing to note about these timelines is that the work over time looks like a step function. We work, full-time, until one bright day we reach FI, and then we can choose to stop working altogether. In reality, stopping to work this abruptly seems to me to have some downsides.

![](</images/W(t)%20step%20function.png>)

This is the timeline graph of a person saving 50% of his income, working full-time (the blue line) until his stash (the red line) reaches his FI number, which happens roughly after 17 years. Then this person stops working completely and starts drawing down on his savings.

All graphs were generated using [this google sheet](https://docs.google.com/spreadsheets/d/15J8bcv3VHqNcQ_rfd1GvhFayi39iXCAP8mO1oTRhFuo/edit?usp=sharing).

I believe that's what MMM did himself, and what many of the FIRE community are doing too. Although I don't think MMM meant it as a prescription.

## Financial Independence is a Gradient

When we say "to reach FI", this might put us into an either-or mindset: it's either you're FI already or you're not FI yet. And FI becomes an end-goal to be had.
If however we think of FI as a gradient, and the more FI we are the more options we have in life. Then accordingly we might exercise these options even before "reaching FI".

Now, let's imagine that someone, Bob, has some control over W(t), and can for example choose to work less than 100% (aka 'full-time'). Will Bob benefit from designing a different career timeline (W(t)) than the above step function?

I started playing around with this idea, myself having designed a different path than the traditional full-time employment one.

Let's first take a look at some options, and later we'll have a deeper discussion about the implications.

## Coast FI

One such way of exercising these options before being fully FI, is called "Coast FI".

!!ref

## Proportion the Work to the Stash

If Bob wants to exercise his options before being fully FI, one option is to proportion W(t) to S.
My thought process is:

-   Ideally, `W(t)` should gradually decrease from 100% to 0%; One way to think about this is: Bob's last day of work should already look similar to retirement.
-   Each year, Bob can choose `W` (how much work to do during the year) according to his current Stash

Here's one equation that satisfies the above: `W=1-S/FI`, where `W` is the proportion of work, `FI` is Bob's target net worth number to retire with and `S` is his Stash (his current net worth)

Assuming Bob starts off with `SR=50%` and `S=0`, and he can control `W` to a decimal precision, we get:

![](</images/<W(t)%20continuous%20no%20slope.png>>)

Oops, looks like Bob has many decades of calculations before him.
Let's iterate on this a bit more.

## W Quantization

While in theory it's plausible that Bob could control W to a decimal precision, we could add the assumption that work can only be reduced in chunks. One example - Bob starts out working 5 days a week (100%), and later reduces W by going 4 days a week (80%), and then 3 (60%), etc.

Now the graph looks like this:

![](</images/<W(t)%20quantization%20by%20days-per-week.png>>)

And Bob sees some light at the end of a 33 year work tunnel. (Note that it's approximately twice the time it would take him the MMM way - 17 years)

Maybe, instead of days-per-week, Bob reduces W by taking mini-retirements, 6 months every year (50%). This now gives the following picture:

![](</images/<W(t)%20quantization%20by%20half.png>>)

Comparing to the MMM graph we clearly see a trade-off: Bob could go half-time 7 years before the MMM way, and fully retire 8 years after it.

## A Middle Ground

Let's make the math a bit more nuanced in search for a middle ground between the two approaches. Our previous equation was:

```
W=1-S/FI
```

Now consider:

```
W=1-G*S/FI
```

Where `G` is our "middle-ground factor", a number between 0 and 1.

Notice:

-   `W` will still start at 100% for `S=0` (zero net-worth)
-   The day before retirement (`S=FI`), `W=1-G`
-   Choosing `G=1` gives us back our previous graph: `W=1-S/FI`
-   Choosing `G=0` gives us back MMM's graph: `W(t)=1`

Now, Bob can adust his own trade-off between the two approaches, by plugging-in his own preferred `G`. For example when `G=0.6=60%`, the graph looks like:

![](</images/W(t)%20G=0.6.png>)

In words:

-   Bob starts off working full-time, 5 days a week
-   On year 8 Bob goes 4 days a week
-   On year 14, down to 3 days a week
-   On year 21, Bob fully retires

## Discussion

I think the most pressing question at this point is **"Why?"**

> Why would we want to cut back on work before fully reaching FI?
