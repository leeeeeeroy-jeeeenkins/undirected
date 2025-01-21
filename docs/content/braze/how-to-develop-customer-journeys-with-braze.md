---
slug: how-to-develop-customer-journeys-with-braze
title: How to Develop Customer Journeys with Braze
authors: [undirected]
---


# How to Develop Customer Journeys with Braze

I'll never forget when we first stumbled upon the enchanting world of Braze. It was a rainy Tuesday, and the office coffee machine was, once again, on strike. We sat hunched over lukewarm mugs of instant coffee, grumbling about the latest marketing fiasco. Little did we know, our stormy Tuesday was about to clear into a ray of customer journey sunshine.

At first, Braze seemed like just another tool in our overflowing box of digital solutions. But, oh - how wrong we were! It was like finding the secret passage in a cluttered attic, leading to rooms full of possibilities. Within weeks, our team's customer communication strategy was not just improved; it was revolutionized.

## Opening the Gateway

The initial steps into Braze felt like stepping onto a stage without a script. Will we dazzle or fumble? We figured the best way to conquer was to start small. There was a coffee stain on Dave's notebook as he scribbled, “Define Objectives.” Sounds straightforward, right? Yet, it was a game changer—our North Star.

Defining a clear purpose before crafting any customer journey is akin to knowing your destination before embarking on a road trip. Imagine Mary, convinced she could reach the Grand Canyon without a map or GPS. She ended up at a miniature golf park. Just like Mary’s detour, not having a clear goal could land us in the most unexpected of places.

Once we hashed out our objectives—be it boosting user retention or cart recovery—Braze started to reveal its charm.

## Mapping the Maze

Next step was mapping out our customer journey, a task not unlike assembling a flat-pack wardrobe with instructions in Swahili. There was heated debate over touchpoints, channels, and why last night's leftovers aren't breakfast, but mapping it all out on paper opened up our minds to potential pathways personalized for our unique audience.

What made it easier was Braze's ‘Canvas Flow.’ This feature provided a visual treat and made crafting the multifaceted route flow with ease, like a paint-by-numbers set for customer interactions. We linked email newsletters to in-app messages and SMS nudges like a string of Christmas lights, taking note to avoid too much flash—no one likes an interruption overload, even in festive winter gear.

### Code the Moments

Herein lies the slice of tech magic that Braze held in its linchpin. We realized how triggered paths could orchestrate an operatic crescendo of engagement. There was Gary, fumbling with his sweatshirt hood while trying to explain “Event-Triggered Messages.” “Think of them like fancy invitations,” he nodded knowingly.

With Braze, these could be an abandoned cart, sage reminders, or a triumphant user milestone—and how we could build these into our schema was a revelation. Like secret codes handed between the graffitied walls of teenage meeting points, they delivered messages our audience didn't even realize they needed until they did.

#### Code Snippet for Trigger Setup:

```javascript
const event_properties = {
  "event_name": "purchase_complete",
  "user_email": "example@domain.com"
};

braze.logCustomEvent("Event Name", event_properties);
```

Our code was not crafted in clean, quiet rooms—it was catastrophic chaos with post-it notes and midnight oil. Oh, the sheer excitement when it finally worked though—we might as well have invented fire anew.

## Crafting Content to Connect

Oh, the copy! Our wild and wondrous wordplay hit new heights in Braze. Initially, our excitement was tempered by the realization that brazen verbosity should be shelved in favor of pithy prose tailored for diverse channels. Like artisanal chocolates crafted with care, each message could be a sweet treat for our audience.

Katie launched into metaphorical overdrive, a frenzied flash of Creative Cloud color palettes and sketches—more exuberant than her dog when spotting a squirrel. She depicted stories in snippets, where every word was steeped in purpose and tied neatly back to our initial objectives. Personalization tags and dynamic content became our allies, allowing each message to resonate with individual spark.

### Dynamic Content Example in Braze:

```liquid
{{#if user.first_name }}Hi {{user.first_name}},{{else}}Hello,{{/if}} Welcome back to our community!
```

Every piece that left our laptops had the warmth of a handwritten note from an old friend; not just a salutation designed for everyone and, consequently, no one. Our content started resembling a homemade blanket, both comforting and dear.

## Testing the Waters

No great odyssey happens in isolation—or without the occasional iceberg. We learned this while immersing our journeys in a sea of QA. Here, A/B testing and experimentation became our guiding stars. Like throwing spaghetti at a wall, and seeing what sticks (we hoped it was pasta), our tests informed our strategy.

There was Colin, with his unruly beard and even wilder theories on engagement timing. But, when we closely monitored user flow and heatmaps, his ah-has became our derisive “aha, indeed!” We tweaked our assumptions and assumptions needed tweaking—our user data had a voice, and we now knew how to listen.

## Analyzing the Aftermath

Ah, the after-show. Imagine the Rolling Stones, gathering post-show to discuss each riff. That was us, analyzing metrics like proud yet anxious parents on report card day. The beauty of Braze's comprehensive analytics? It laid bare our strengths and hiccups, without the need for clandestine deciphering like we were members of a secretive club.

Conversion rates, engagement peaks, and the dreaded churn probability—all served up in Braze's bouquets of data. We realized it was our duty to celebrate wins, no matter how modest, and approach setbacks with curiosity and a strategic scalpel.

## Reflect and Refine

They say: if you want to go fast, travel alone. If you want to go far, go together. Our Braze adventure was intricate and layered like a seven-course meal; and as any esteemed head chef does, we gathered feedback to perfect our menu. Continuous improvement became our mantra, with every journey maturing it reminded us of a fine wine.

Feedback from our users? That was the golden goose. We surveyed, we listened. Their stories became the stories we penned back to them. Forevermore, the cycle continued.

### Summary

So, there you have it, unfolding just as it once did for us. The versatile grand tapestry of Braze is there to enable us to craft customer journeys that do more than just cover the distance; they enrich every step of the way.

We emerged from our Braze voyage not just as travelers of the digital landscape but as confident navigators. We've torn down metaphorical cluttered attics, and replaced them with rooms of possibility—that once elusive, now within our grasp.

In closing, our word for Braze is thus: transformative. Now, about that damn coffee machine.