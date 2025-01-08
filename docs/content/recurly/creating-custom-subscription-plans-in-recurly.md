---
slug: creating-custom-subscription-plans-in-recurly
title: Creating Custom Subscription Plans in Recurly
authors: [undirected]
---


# Creating Custom Subscription Plans in Recurly: A Journey of Discovery

You know that feeling you get when you first unwrap a brand-new gadget? Your heart races, there's an intoxicating mix of possibilities swirling in your mind, and you're filled with the naïveté of discovery. That's the exact sensation we experienced the day we decided – a tad impulsively – to dive headfirst into creating custom subscription plans using Recurly. Our objective was laser-focused yet vast: to create a delightful subscription experience for our customers online. We promised ourselves no jargon, no pretension, only pure distilled delight in discovery, and what a ride it's been.

## Setting the Stage: A Story of Curiosity and Courage

It all began on a rainy Wednesday afternoon – those characteristically dreary hours when the mind starts to wander beyond the confines of its routine. We were perched at Starbucks, laptops open, caffeine leading the charge. My partner, Alex, threw a question into the digital ether: “What if our subscriptions didn’t suck?” A bold query indeed, one that sounded like a challenge to invoke open-source magic and shake up our offerings with Recurly’s prowess.

### Enter Recurly: The Wizardry Box

Recurly, as you might imagine, is like a mysterious box of wands for the modern business magician – allowing you to weave together subscription schemes that can delight or infuriate depending on your skill level. It doesn't scream complexity, nor does it whisper simplicity, but beckons warmly like a friend with a secret.

Let's do this together, I remember thinking. We logged into Recurly for the first time, and those brave enough to venture forth with us emerged, like Dorothy stepping into Technicolor Oz. Bright and bewildering with possibilities.

## Step One: Charting Our Course

Before embarking on the subscription path, we had to sketch our goals — a rough map, if you will. What kind of journey were we setting forth? What magical items would our customers want to carry along? We began with: 

1. **Identify the Audience**: Who are they? What do they desire in their deepest of hearts? Knowing your subscribers (almost like knowing which friends take milk and which abhor it) makes a world of difference.
   
2. **Decide the Offerings**: Basic plan, premium options, or perhaps something mad like a bespoke tier named after a cat? The world's our oyster, and the pearl is waiting.
   
3. **Determine Billing Cycles**: Monthly, yearly, or travel bravely where few dare – variable billing!

It was quickly clear that our minds needed to stretch over this vast landscape — ideas flowing, caffeine invigorating our march through discussions that seemed daunting at first but also exhilarating.

## The Building Blocks: Harnessing Recurly’s Magic

The next morning, we sipped Earl Grey and recalled our creation scheme, the plan ready but needing form. We opened Recurly once again. 

### Setting Up a Plan

Here's where things started crackling with creativity and coding alike:

- **Navigate**: From the Recurly admin dashboard, we scooted over to the 'Plans' section. It was like approaching a garden, each plant waiting to be pruned or plucked.
  
- **Create a New Plan**: Like placing the first brushstroke on canvas. We tapped the 'New Plan' button, filling in the essentials: name, code, description – just like naming a new band that could change the world, or at least your tiny corner of it.
   
- **Define Pricing**: Choosing a price was an art and a science. Too low, and we're as undervalued as a dollar store Picasso; too high, and we'd frighten customers faster than you can say avant-garde.
  
- **Set Billing Interval**: Here comes the juicy bit. We chose our frequency. It’s like setting a metronome in a symphony – does this symphony live every month, year, or somewhere off the beaten path?
  
- **Trial Periods and Set-ups**: Oh, this was akin to offering a plush chocolate sample before unlocking the vault. We set up trial periods, thinking of them as keys to customer engagement and satisfaction with first bites and little nudges forward.

Executing these steps was anything but a lonely task; we chatted away as two birds building a nest in perfect unison, occasionally veering off topic into the most pleasant of absurdities.

#### Code Snippet Collaboration

Of course, sprinkling some code made it enchanting, and Recurly’s API had our backs. Here's a glimpse of what we did in the console:

```javascript
const recurly = require('recurly');

recurly.Plan.create({
  plan_code: 'premium_plan',
  name: 'Premium Subscription',
  interval_unit: 'months',
  interval_length: 1,
  setup_fee_in_cents: 2000,
  trial_length_days: 30,
  unit_amount_in_cents: {
    'USD': 2000
  }
}, function (err, plan) {
  if (err) {
    console.error('Plan creation failed', err);
  } else {
    console.log('Plan created successfully', plan);
  }
});
```

A masterpiece in its tiny frame, realizable and beautiful, much like our afternoon espresso ritual.

## Taming the Beasts: Fine-Tuning and Testing

Time stretched on, and we returned to our labors, crossing the bridge from concept to reality. Testing was crucial – Alex and I were like exquisite chefs tasting every possible note of flavor before opening the restaurant doors at dawn.

- **Simulating Subscriber Experience**: By using our internal team as beta-testers (voluntold turns to volunteer here nicely), we sought knowledge.
  
- **Gauging Metrics**: Analysing whether our plans were drawing the customer sweetened water or bitter pith. Adjustments were more common than we’d anticipated.

Throughout this process, we learned a valuable lesson: never underestimate the detail in the dashboard, nor the power of feedback.

## Conclusion: Sharing the Magic

At the end of this wondrous journey, equipped with newfound knowledge like traveling minstrels ready to share our tales, we grasped one truth: creating custom subscription plans in Recurly involves art and logic, creativity and analytics, joy, along with no small amount of work. Yet, the empowerment we felt at facilitating our own customer's journey—an experience that was bespoke and aligned with our vision—made every coffee-fueled night worthwhile.

There we stood, blinking into the dawn of a new realm where subscriber experiences danced to our tune, orchestrated with insight and ingenuity gifted from Recurly. Was the effort worthwhile? Absolutely. And next time? Well, now we're ready. Ready to weave new stories, rethink the rules, and dare to dwell in the realm of subscription wonders once more.