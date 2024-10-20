---
slug: step-by-step-approach-to-configure-pricing-in-salesforce-cpq
title: Step by Step Approach to Configure Pricing in Salesforce CPQ
authors: [undirected]
---


# Step by Step Approach to Configure Pricing in Salesforce CPQ

Ah, Salesforce CPQ. The labyrinth of business software that baffles and beguiles us in equal measure. I remember my first time diving into this maelstrom of pricing and configuration, and let me tell you, it felt like trying to navigate a corn maze in the dark after swapping your compass for a cucumber sandwich—utterly bewildering. Tony from sales, bless his heart, was going to combust if we couldn’t decipher the mysteries of CPQ to price his beloved widgets before the upcoming sales meeting. Little did I know, this would become one of those adventures we'd later recount with a mix of amazement and “Can you believe we did it?” pride.

Each section below will share fragments of that journey, illuminating our path with every revelation.

## Step 1: Understanding Product Bundles and Pricing Logic

Before we engaged with the beast that is Salesforce CPQ, we learned a vital lesson: coffee helps. But aside from that, you must comprehend the basics—like the concept of product bundles and pricing logic. So there we were, fueled by caffeine, squinting at our screens like deciphering ancient runes.

In CPQ, product bundles let you package multiple products together, while pricing logic determines how these products are priced. Imagine a burger combo meal—you get a burger, fries, and a drink for a single price. It's essential to set your mind to think in these terms.

### Action Steps:

1. **Identify your products**: Know what you’re selling. Yes, it’s obvious, but you’d be surprised—like the time we had no idea why Tony’s “Invisible Widget” wasn’t showing any sales.
  
2. **Define your bundles**: Go to the Salesforce CPQ home page and navigate to Products. Look for the "New Product" button, a sparkling beacon in the sea of buttons.

3. **Set pricing logic**: Choose a pricing method that suits your bundle. Decide if you're offering a discount, a flat rate, or even pay-per-hug—we didn’t go that far, but you get the idea. The choice is under the “Pricing Method” field.

That’s how we started sketching the puzzle, telling Tony, "See? The ‘Invisible Widget’ can indeed be priced. It just needs imagination and a splash of setup."

## Step 2: Pricing Methods: An Art and a Science

Now, why on Earth does Salesforce give us more pricing methods than a pizza joint has topping combinations? It's both maddening and grand. We learned that choosing the right pricing method is akin to picking the right sauce for your pasta—they will make or break the dish.

### Action Steps:

1. **List Price**: The vanilla of pricing methods. It’s the standard price you find in your pricing book, that oft-forgotten tome gathering dust in sales cubicles.

2. **Cost Plus Markup**: We chuckled how this method secretly speaks the language of salespeople exaggerating their prowess—add a markup to the cost, like adding 10% extra to your story of catching a fish.

3. **Block Pricing**: Picture a bracket where consuming up to X units costs Y. We imagined pricing Tony’s widgets by the dozen, pondering if a 'baker's dozen pricing' should be a thing.

4. **Tiered Pricing**: Discounts based on volume. The more you buy, the less you pay per unit—you know, like every late-night TV ad ever.

5. **Option Pricing**: Sometimes, fancy isn’t better, and you just want to offer ‘select’ options with unique prices. Simplicity can be an art form, truly.

Our clowning around with block and tiered pricing felt like mixing a magic potion, but once you taste the elixir, it makes the KISS principle (“Keep It Simple, Stupid”) seem genius.

## Step 3: Choose Your Price Books Wisely

You might say, “A price book? Sounds dusty.” It does. But in Salesforce CPQ, it’s more like a glitter-covered grimoire—housing all your pricing secrets, waiting to spring to life in a sales meeting.

### Action Steps:

1. **Create a Price Book**: Navigate to the elusive “Price Books” tab. If it’s hiding—go to App Launcher. There, create a new price book, gild it with a suitable name, and whisper a secret wish into the ether. That last part might be optional.

2. **Add Products to Your Price Book**: No gaping voids here. Click on "Add Products" to mix your golden blend. Choose your pricing from the aforementioned bewildering options—imagine Tony’s delight seeing his widgets listed with prices that make sense.

3. **Activate the Price Book**: If a price book falls in the forest and no one hears it...right. Always activate it to echo through Salesforce.

Our shared epiphany was that these price books are like ever-growing recipes for success; they must be defined, revised, and cherished.

## Step 4: Discount Schedules – The Art of Persuasion

Ah, discounts. The siren song that lures customers into purchasing more than they intended. It's an art form, balancing profit margins with irresistible incentives.

### Action Steps:

1. **Set Up Discount Schedules**: Under "Discount Schedules," begin anew. Name it after your most tempting offer—like Tony’s “What a Steal” widget discount.

2. **Define Discount Tiers**: Pose as a sales swami and create tiers. Picture a world where ordering 50 widgets gets a better deal than 10—magic.

3. **Attach to Products/Price Books**: We attached the discount schedule to the price book, solidifying Tony’s pitch with persuasive savings.

Discount schedules are like when you finally understand origami. Complex? Yes. Confusing? Sometimes. Yet, when properly folded, they’re a powerful tool that can transform your sales process.

## Step 5: Guided Selling – Making It Customer-Centric

Guided selling in Salesforce CPQ is perhaps the most charming feature. It's like holding customers' hands, leading them toward the most optimal choices without salesy jargon.

### Action Steps:

1. **Create Guided Selling Processes**: Under "Guided Selling Processes," add a new one. Simple name, grand strategy.

2. **Define the Questions and Filters**: Akin to being a choice architect, crafted questions lead your customers to the sale, softly enlightening their path.

3. **Deploy Guided Selling**: Assign it to specific quote processes. Evangelize the tales of Tony's widgets, helping customers understand their true value under your skillfully programmed assistance.

That’s when Tony’s appreciation turned into a round of applause. Who knew we’d get our customers to self-discovery with our guided paths?

## Reflections and Revelry

Each step, each head-scratching moment bundled with flashes of insight, grew into a well-rounded understanding of Salesforce CPQ's pricing features. Time and again, Tony emerged as our grounding mascot, cheering on our every move, his delight a barometer of our success.

In the end, was it easy? Not at first. Did we laugh, cry, and have a few existential crises along the way? Yes. But, it was fleeting discomfort for the greater good—a revelation of the intricacies Salesforce CPQ offers. 

When you step back to admire the configured masterpiece, you realize it encapsulates far more than numbers—it’s a symphony of logic, user-friendly design, and strategic genius. 

As we closed our laptops with pride, Tony promised endless doughnuts for the team's dedication. And not just any doughnuts—the good ones with sprinkles and the occasional surprise filling, similar to the surprises we uncovered in CPQ’s realm.

And my, what a sweet climax that was—because we earned those sprinkles, with every bit of confounding, exhilarating, downright joyful experience Salesforce CPQ threw our way!