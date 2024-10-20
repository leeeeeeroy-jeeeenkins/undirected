---
slug: how-to-configure-multi-currency-in-salesforce-cpq
title: How to Configure Multi Currency in Salesforce CPQ
authors: [undirected]
---


# How to Configure Multi Currency in Salesforce CPQ

## A Journey into the Currency Jungle

Once upon a particularly drizzly Tuesday afternoon, I found myself sipping a lukewarm cup of coffee gazing at the endless rows of numbers glaring back at me from my computer screen. It was one of those rare moments when you feel gossiping with your reflection might be more productive than deciphering Exchange Rate logic in Salesforce CPQ. My colleague, the ever-chipper Ellen, had sidled over casually, laden with three grapefruits (don’t ask) and a glint of excitement only matched by that time she had discovered a new bakery down the street. 

“Hey, have you ever tried configuring the multi-currency setup in Salesforce CPQ?” she chirruped. “Seems like a fun puzzle!” 

Fun was not the word I had in mind, yet here I was, in the weeds of currency configuration needing also to stop myself from sinking into the abyss of infinitely nested Salesforce screens.

Let us embark on this configurational journey together, enveloped in both confusion and ultimate triumph, as we explore the adventure of multi-currency configurations in Salesforce CPQ.

### Getting Our Feet Wet

Before we dive head-first into a currency-laden sea, it's crucial to summon the magical beings known in business worlds as Currency Locale preferences and Exchange Rates. I remember this like it was yesterday, Ellen beside me harmonizing to the whir of computer fans. The key to swimming rather than sinking lies in finding our way to the setup area.

1. **Enable Multi-Currency:** First, we dip our toes in by navigating to **Setup** from the Salesforce CPQ app. Type `Company Information` in the Quick Find box. Tread carefully because once you enable this, there’s no going back. Click **Edit** and select the **Activate Multiple Currencies** checkbox. Magic.

2. **Set Corporate Currency:** The next step involves choosing our almighty default currency, known decoratively as the Corporate Currency. It's like picking your Hogwarts house, but in finance form. Go back to **Company Information**, find **Organizational Defaults**, and select your ideal currency. 

3. **Adding Additional Currencies:** Now, much like gathering a motley crew for a heist, navigate to **Manage Currencies**. Here is where the adventure begins: click **New** and add the currencies that make your offering worldwide—don’t forget the Exchange Rates (preferably up-to-date). Ellen, with all the glee of a squirrel finding an unsupervised picnic, was quite particular about regularly updating these rates.

### Deep Dive into Currency Configurations

As I sat perched at my desk, a narrative weaving in my head that currency configuration maps suspiciously well into an epic quest, a fairy godmother of sorts introduced herself in the form of dynamic currency settings. "Remember context!" she screeched—the same advice given by my grandmother, perhaps as pertinent in currencies as it was in her love stories.

1. **Configure Exchange Rates:** Time to get friendly with math. In the **Manage Currencies** page, to adjust or add Exchange Rates (the lifeblood of currency conversion), click on **Manage Exchange Rates**. You’ll dance the tango of entering, updating, and saving your current rates here. 

2. **Create Price Books in Multiple Currencies:** Our next hurdle is to offer product prices for the world to see – quite literally. In CPQ, you want to operationalize products in glorious multiple currencies. Beneath the umbrella of **Standard Price Book**, create additional Price Books for each currency. When Ellen and I reached this stage, we celebrated with a grapefruit—juice dripping down my keyboard, but a small price for success.

3. **Assign Currency to Products:** Products, dear friends, follow their own rules. Navigate to **Products**, then under each Product Detail, add** Price Book Entries** with your shiny new multi-currencies. Here you enter your local prices, making sure each product’s currency is accurate.

### Wrangling the Final Beasts

The complexity lied not in individual tasks but in ensuring none of our efforts contradicted some unseen law of currency fellowship. I found myself often untangling rogue strings just to make sense of our entries.

1. **Manage User Currency Settings:** Each user should have the currency that speaks to them. Find **Users** under Setup, and ensure everyone has their locales set—just in case someone fancies INR over USD.

2. **Adjust Opportunity Currencies:** Opportunities thrive in diversity. When creating Opportunities, ensure their currencies match client preferences. There’s nothing worse than upsetting a Parisian with dollars when they requested euros for their escargot export.

3. **Implement Currency Conversion Logic in Quotes:** Here, Ellen and I had our most philosophical discussions over tender meanings of foreign exchange losses, quoting Oscar Wilde. Utilize **Quote Templates**—which we found in CPQ under the odd tab of fun—to present consistent and accurate currency information to clients.

### The Sunset of Currency Configurations

With our journey’s end nearly visible, I often wondered how many metaphorical mountains we climbed or how much caffeine we ingested. Our adventure wasn’t without hitches—rogue decimals appeared, threatening chaos, but our perseverance held fast against all odds.

Envision gathering a trove of insights, like explorers returning with knowledge to benefit the village. This voyage into configuring multi-currency within Salesforce CPQ taught us not only intricacies of digital finance but the rarely charted course of teamwork, laughter, and yes, even the adventures of grapefruits.

May your own currency endeavors prove fruitful too, and as Ellen insists we part with advice: "Never work with outdated exchange rates..." a saying that should perhaps extend beyond Salesforce.

Happy configuring!