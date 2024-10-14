---
slug: how-to-set-up-conversion-tracking-in-google-ads
title: How to Set Up Conversion Tracking in Google Ads
authors: [undirected]
---

# How to Set Up Conversion Tracking in Google Ads

It was a crisp Tuesday when we first dove headlong into the labyrinthine depths of Google Ads. We, being blissfully unaware of what lay ahead, clicked through countless tabs with reckless abandon, until we found ourselves wondering—are these ads really making a difference? It was Mike, our coffee-addicted coder, who asked the golden question, "How do we know if this is actually working?" This, my friends, is where our tale of tracking conversions begins.

## Step 1: Define Your Conversions

Picture us mulling over donuts and coffee, deciding what really mattered in our digital kingdom. What Fandango would mark a success? Sales? Sign-ups? We realized that defining a conversion was akin to deciding what "winning" meant in Monopoly (pro tip: always buy the railroads). So, before fiddling with Google Ads, pick your conversion goal like it's the last scoop of your favorite ice cream.

## Step 2: Create a Conversion Action

With our conversion dreams outlined, we ventured into the belly of Google Ads. But first, a confession—we got lost. Here's a smoother path:

- **Log into Google Ads**: Easy peasy.
- **Click on ‘Tools & Settings’**: It's the wrench icon, which sounds mechanical, but promises wonders.
- **Choose ‘Conversions’**: Think of this as your digital vault of victory.
- **Hit the ‘+’ Button**: This is where magic begins—we promise it's not forbidden.

Select an action, be it website, app, phone call, or import. We opted for "website"—we are simple folk.

## Step 3: Set Valuable Parameters

Mike pondered as he added a price tag to our digital dreams. We chose a monetary value for each conversion. Remember, numbers should reflect significance in your strategy. We recommend not choosing `7.38` just because it's your lucky number.

- **Conversion Name**: "Victory!" we mused.
- **Category**: Take your pick—purchase, lead, signup, etc.
- **Value**: Be realistic; no unicorns here.
- **Count**: Every conversion or just one—choose wisely, young Padawan.

## Step 4: Install the Conversion Tracking Tag

This is where Mike, fueled by his espresso shot, felt at home—code blocks and all. By adding some lightweight JavaScript to our website, we finally crossed into the promised land of tracking.

Copy the code Google provides, something like this:

```html
<!-- Global site tag (gtag.js) - Google Ads: xxxxxx -->
<script async src="https://www.googletagmanager.com/gtag/js?id=AW-XXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'AW-XXXXXX');
  gtag('event', 'conversion', {'send_to': 'AW-XXXXXX/XXXXXX'});
</script>
```

Insert it before the `<head>` tag closes. If you're not inclined to dabble in code, seek comfort in plugins that save you from HTML heartburn.

## Step 5: Test and Confirm

There's little joy like watching your efforts unfurl. Navigate within Google Ads back to ‘Tools & Settings’, the same place we started, click 'Conversions', and check your action status. We hit "Record Result!" as if it were a home run.

## Celebrate Your Victories 🎉

Like triumphant knights, we sat back, grinning over our attempt at demystifying conversion tracking. Google Ads tracking isn't just a gateway to understanding your audience but a powerful realization of how your business narratives resonate in digital echoes. Implement, observe, tweak, and may your conversions be fruitful.

And, just as we savored the last sip of our drinks that Tuesday, we encourage you to take a moment to relish what you've created. Cheers to success and the simple joy of learning together!