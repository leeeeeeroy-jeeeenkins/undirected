---
slug: how-to-customize-product-bundles-in-salesforce-cpq
title: How to Customize Product Bundles in Salesforce CPQ
authors: [undirected]
---


# How to Customize Product Bundles in Salesforce CPQ

Ah, those chilly spring mornings, when I’d watch the dew glint off my kitchen window while sipping a lukewarm coffee. It was on one of these mornings, laptop screen glowing with the brightness only a naive nine-to-fiver can muster at 6 a.m., that I stumbled upon an anomaly in our Salesforce CPQ setup. Our team had messed around with product bundles, and it felt as messy as a squirrel at a rave. I had the honor—nay, the privilege—of unraveling it like a peculiar digital matryoshka doll. 

## The Beginning: Unravelling the Bundle

Imagine discovering your favorite childhood game—hide and seek—but with business products. Salesforce CPQ allows you to piece together product bundles just like that. These aren't just random assortments; they're symphonic concoctions of related items that need to be bought in tandem. Think of them as carefully curated mixtapes for your sales strategy, each track a product that’s meant to groove together in perfect harmony.

But how do we customize, you ask? Let's set the stage. First, picture a night of spreadsheets and some soft jazz. Now, to our first steps:

First things first, we hit the **Product** tab, our doorway into the realm of possibilities. We select `Product Bundles`, which is like picking up that unlabeled vinyl you just *know* is going to be gold. Then, it's time to hit **New**.

A window appears. It’s a blank canvas waiting for our touch—here, it's crucial to note the *Product Family* because everything needs kinship, right? Enter a name for your bundle. You want something catchy—a name that’d make even your skeptical uncle nod in approval.

## The Anatomy of Components: Crafting with Care

Ah, components. The bundle's bread and butter, or grape jelly if you're feeling rebellious. Adding components feels like assembling the perfect snack platter. Here's how it unfolds:

1. **Related Lists Galore:** On your product detail page, the Related Lists section is your smorgasbord. Choose **Options**.

2. **Add New:** Initiate the magic by clicking on "New Product" under Options. Give it a name - smart names pay off here - and define it. *Is it optional? Required?* Custom settings are our friends.

3. **Quantity:** Set the default quantity to ensure sales aren't left high and dry - nor is the warehouse overflowing with unnecessary widgets.

4. **Min/Max Limits:** Here’s a safety net, a gentle reminder that sometimes too much of something is too much. Set these thoughtfully.

5. **Shields Up—Rules:** Remember the time Aunt Margery baked a pie? But whoa, it needed custard, and custard alone. Bundle rules ensure your bundle needs and gets what's crucial. In Salesforce, these rules govern required choices, enabling dependencies, preventing mishaps. Navigate to **Configuration Rules**.

   ```markdown
   Rule Name: Custard for Pie
   Rule Type: Selection
   Quote Process: Volunteer Pie Baking
   ```
   
## The Artful Dodger: Custom Actions and Filters

Our morning coffee meetings often began with head-scratchers about navigating Salesforce like stealthy raccoons tiptoeing through someone's trash can. Custom actions in CPQ are your raccoon eyes—focusing through the chaos. They allow you to guide users through the bundle maze without them wandering off.

- **Navigate to Custom Actions:** Twirl into this section like a dance move. Enter a name worth remembering, like a favorite dance track that ensures rhythm in chaos. Select types—*Button* typically does the trick if directing traffic.

- **Filters:** You wouldn't wear every item from your closet at once, as flashy as that might be. Filters customize configurations, providing users a lens to view only what matters. It's like a magical wardrobe assistant.

## The Test Drive: Ensure it Purrs

Before introducing a new vehicle to the autobahn, you ensure it, you know, works. The same applies to our creation. Testing bundles makes sure it hums smoothly without any grinding gears:

- **Quote Creation:** Use various scenarios. No two clients are the same, much like snowflakes or left socks. Quoting is the dessert video in your cooking channel—preparing for the big reveal. 

- **Validation and Error Panels:** These panels will hint if you've added pineapples on your pizza without authorization. Check for warnings, errors, or that hollow feeling when you've forgotten something.

## Real Talk: Lessons in the Spreadsheet Vine

The gold-tinted glow of spreadsheets and snarky office banter taught me more than customization—like how not to forget about pricing strategies. Embedding all this knowledge into bundles is as important as checking if you remembered to lock the door when you left home. 

Our shared journey through Salesforce CPQ customization was an exciting tale of discovering limits—and then yearning to surpass them, together. It’s uncanny that through customizing these bundles, we weren't just assembling products; we were building bridges of understanding, strengthening our ideas about teamwork—and maybe, the occasional friendly rivalry over the office foosball table.

Now remember, as you sail on your CPQ journey—every bundle tells a story, and *you* are its author. Embrace the quirks, see the beauty in their complexity, and above all, don’t forget to enjoy a lukewarm coffee now and then.