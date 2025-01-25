---
slug: implementing-advanced-dunning-strategies-in-chargify-to-recover-lost-revenue
title: Implementing Advanced Dunning Strategies in Chargify to Recover Lost Revenue
authors: [undirected]
---


# Implementing Advanced Dunning Strategies in Chargify to Recover Lost Revenue

Ah, the art of dunning. It’s like a gentle reminder mixed with a sprinkle of persistence — a dance most of us hope to master but find ourselves stepping on toes now and again. There I was, at Johnny’s Coffee House, sipping a latte that was way too hipster for its own good, when I first encountered the dreaded "Payment Failed" alert. For anyone else, it might have just been an email, but for me, it was a war cry. My business was bleeding cash because of failed payments, and I wasn't going to just sip away my troubles.

## Our Rocky Start with Chargify

Let’s face it, dunning sounds oddly delightful, doesn’t it? Until it knocks you upside the head with a reality check on recurring revenue. During one of those caffeine-induced revelations, we (my small and mighty team) decided it was time for Chargify to step up its game. Little did we know, the solution was as layered as a mille-feuille — requiring patience, persistence, and a pinch of pluck. Our goal: recover that lost revenue with precision and flair.

### Identify the Invisible Cash - An Awareness Mission

First, we needed to get cozy with our data. Jerry, our numbers guy with a penchant for spreadsheets, dove into our subscriber stats. At first, it was like staring into a whirlwind of numbers — so dizzying it could make even an accountant’s eyes cross. But Jerry, bless him, found the key: understanding the patterns of failed payments. We had a blind spot, and identifying it was our first eureka moment. Essentially, we were Indiana Jones, and Chargify was our map to the treasure.

Let’s get nerdy here: run a deep analysis on your billing data to spot discrepancies. You’ll need some specific code that extracts failed transactions. Something like this:

```python
import chargify

def get_failed_payments():
    failed_list = []
    subscribers = chargify.get_subscribers()
    for sub in subscribers:
        if sub['payment_status'] == 'failed':
            failed_list.append(sub)
    return failed_list

failed_payments = get_failed_payments()
print(f"Failed Transactions: {len(failed_payments)}")
```
Once we had our dirty little list of failed payments, it was time to act.

### Crafting the Perfect Reminder – A Gentle Nudge

You know how every family has its go-to comforting meal? Ours was spaghetti bolognese — failsafe, reliable, mmm. We needed the digital equivalent to warm, soothing reminders. We drafted our first email with compassionate, yet firm language. Trust me, writing these emails is an art. You need a dash of empathy, a sprinkle of urgency, but with a whole lotta tact so your customer doesn't feel you're poking them with a stick.

We ran a pilot test where the results surprised us. Turns out, a personalized first line and a light-hearted touch increased our response rates significantly. Just like that, our dunning emails evolved, channeling the kind of warmth you feel when a friend offers to buy you coffee because, dang it, it's been one of those days.

### Rolling with Failed Payments - A Plan of Action

Charge after charge — hmmm, a name for Chargify, I wonder if that’s intentional? — we decided to stay on top of notifications. Notifications are to Customer Success Reps what bread crumbs are to Hansel and Gretel. Chargify’s notification feature is more like a siren than a breadcrumb when configured correctly, alerting you immediately about the dreaded decline.

Set up alerts in Chargify to notify your team of payment hiccups. Something like:

```shell
chmod +x set_alerts.sh
./set_alerts.sh
```
Ah, troubleshooting. A necessary evil, I suppose. With configured alerts, we were ever-ready to swoop in and save a subscription before it said its last goodbye.

### An Experiment with Schedules – Time’s Powerful Grip

Time is a tricky beast. Strike too soon, and you’re that overly eager high-fiver who can’t take a hint. Wait too long, and your timeline — much like those half-forgotten New Year’s resolutions — fizzles out to nothingness. We decided to stagger our dunning attempts over a set period to maximize impact and realized the magic number was three attempts, over 7, 14, and 21 days. Like planting seeds for future growth, patience here was literally currency.

### Customizing Payment Recovery – Flexibility Wins

Sometimes when you're building a business, it feels like you’re in charge of a pirate crew, constantly navigating treacherous waters. We introduced retry logic in Chargify that allowed for automatic and manual retries. This was our compass, guiding us through stormy seas as our revenue streams found their rhythm again. Chargify’s flexibility in configuring dunning settings — including retry logic — is the beacon we all seek when our ship (business) is lost at sea.

Here's a glimpse into customizing retry intervals:

```python
settings = chargify.get_settings()
settings['dunning']['retry_interval'] = [7, 14, 21] # days
chargify.update_settings(settings)
```

Sounds technical? It’s simpler than it looks, promise.

### Reimagining Our Relationships – The Human Element

During an afternoon walk, we mused about people — our subscribers, our partners, our peers (and maybe the neighborhood cat who has a habit of dropping by to say hello). Remembering that behind every failed payment is a person with a story was crucial. We took this wisdom as inspiration to add personal touch-points through phone calls or personal emails. Imagine my surprise when our subscriber engagement skyrocketed just because we remembered someone’s name. It’s the small things that count, like finding a soggy ten-dollar bill in a forgotten pocket.

### An Ongoing Adventure with Chargify

Reflecting on our journey with Chargify and our newfound dunning prowess, it feels gratifying, akin to finally mastering that sourdough starter. Our mission? Ensuring no revenue slips through unnoticed. There's undeniable joy in knowing you’ve exorcized the payment-failure ghosts from your business. Chargify’s toolset is like that trustworthy Swiss Army Knife that bestows a sense of security. Now, armed with our advanced dunning strategies, we are like digital superheroes ready to tackle payment issues at their source, capes and all.

So, friends, let's raise a metaphorical coffee cup to the power of implementing advanced dunning strategies. Together, let’s unlock those doors and watch as our revenue adventures take flight.

Now, who's up for a coffee?