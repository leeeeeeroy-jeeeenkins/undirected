---
slug: how-to-set-up-a-subscription-plan-in-zuora
title: How to Set Up a Subscription Plan in Zuora
authors: [undirected]
---


# How to Set Up a Subscription Plan in Zuora

Ah, Zuora — the magical land where billing and subscriptions are like a perfectly brewed cup of coffee. You know, the kind where every sip feels just right. A little over a year ago, our tiny startup was like an awkward teenager at a school dance, not quite sure how to handle this whole subscription thing. We needed Zuora to help us glide across the dance floor, and luckily, we weren't stepping on too many toes. The journey was... illuminating. Let's dive into setting up a subscription plan in Zuora, the way we would for our friends gathered around a campfire, complete with marshmallows and a few lighthearted chuckles.

## Unboxing Zuora

Remember when we first opened Zuora? It felt like discovering a treasure chest buried in the attic — dusty, but full of potential. Before we could gleefully dive into the subscription pool, we had to set up our playground. Here's how we did it, with the kind of detail that could inspire a sitcom.

### Step 1: Sign Up and Log In

First things first, we had a mighty sign-up button glaring at us. Like an enigmatic doorway, we pushed through.

- **Create an account**: Navigate to the **Zuora website**, and click that luscious sign-up button. Enter your details like world explorers marking a new territory.
- **Log in**: With our credentials firmly in hand, we logged into Zuora's dashboard. Voila! Now, we were navigating a wonderland of billing solutions.

### Step 2: Explore the Interface

Once inside, we felt like kids in a candy store. So many sections, so little time! We clicked around — all wide-eyed and eager. Here's what we noted:

- **Dashboard**: Our control center. The heart of operations filled with stats and insights.
- **Subscriptions**: The beating pulse — where every new subscription plan would eventually live and breathe. 
- **Settings**: Our toolbox — the land of configurations, the fount of customization.

## Crafting Our First Subscription Plan

Now, dear reader, imagine our excitement when we realized we could finally sculpt our first subscription plan. After all, who doesn't enjoy a little creation?

### Step 1: Navigate to Product Catalog

Much like my grandmother's recipe book, it was time to gather the ingredients.

- **Click on 'Product Catalog'** in the sidebar. It's like finding the secret ingredient in a much-loved dish.

### Step 2: Create a Product

Our product needed a name. Something snappy, inviting. We huddled like poets around a campfire, concocting brilliance.

- **New Product Creation**: Click on *"add a product"* and fill in the details. Name, description, and-cherry on top-pricing.
- **Save it**: Hit save, and just like that, we had our first product! Cue virtual fanfare.

### Step 3: Define the Rate Plan

Products are the soul, but rate plans are their beating heart.

- **Add a Rate Plan**: Within the product, click *"add a rate plan"*. It felt like decorating a cake; this was where pricing, charges, and billing intervals mingled like old friends.
  
Take, for example, our basic plan. We opted for:

  ```yaml
  Basic Plan:
    - Monthly charge: $10
    - Features: Basic access, 24/7 support
  ```

- **Choose a Charge Model**: Flat fee, per unit, or tiered. Each with its quirks, like choosing the right dance partner.

## Subscription Settings

We had the clay, now it was time to sculpt the statue and define the structure — setting up subscriptions that suit our business model like a glove.

### Step 1: Go to 'New Subscription'

A quick trip to the subscriptions tab revealed all pending subscriptions, waiting like puppies in a window.

- **Click 'Create New Subscription'**: Time to unleash the creativity.

### Step 2: Fill in Subscription Details

It was like writing a love letter to our customers — dates, pricing, plans, oh my!

- **Select Account**: Choose the account we would link the subscription to.
- **Select a Product and Rate Plan**: As a master chef selects their finest ingredients.
- **Renewal Terms**: Do we renew monthly like a beloved magazine or annually with a flourish?

### Step 3: Set Up Billing and Payment

Now, we entered the financial labyrinth, armed with a quill and a ledger.

- **Choose a Billing Cycle**: Monthly? Weekly? We chose one that resonated with our financial rhythms — monthly for us.
- **Set Payment Terms**: Like our financial wheel, ready to recoup costs with grace. Net 30 days seemed fair.

## Testing Our Subscription

No creation was complete without testing. It's the final affirmation of our billing ballet.

### Step 1: Create a Test Account

- **Test Accounts**: A sandbox environment, free to explore without financial repercussions. Perfect for unbridled experimentation.

### Step 2: Trial Runs

- **Activate Test Subscriptions**: We progressed from hypothetical to real-world possibilities, activating and watching money flow like sugar in tea-timed cadence, ensuring seamless transitions.

## Reflecting on Zuora's Magic

Having unwound the mystery of Zuora left us breathless. The process of creating, setting up, and executing a subscription plan became not just a task but an experience — one filled with learning, laughter, a few groans of frustration, and sweet, sweet satisfaction.

A memory surfaced, seated around the cluttered desk with pastries and coffee. With hope on one side and determination on the other, we cracked it like an old code. Zuora signup became a rite of passage, and setting up a subscription plan, our testament to teamwork and ingenuity.

The journey still continues. New products, new plans, more elaborate dance steps. Each tangle, twist, and feature explored, with Zuora growing alongside us — an unexpected dance partner becoming a steadfast ally.

With that, my dear fellows of the subscription order, we'd say journey cheerfully into the land of recurring revenue. Embrace the subscription, wield the powerful user's journey, and harness the wizardry of Zuora! 

May your billing be accurate, your subscribers loyal, and your coffee perpetually warm.