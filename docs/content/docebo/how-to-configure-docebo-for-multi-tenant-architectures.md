---
slug: how-to-configure-docebo-for-multi-tenant-architectures
title: How to Configure Docebo for Multi Tenant Architectures
authors: [undirected]
---


# How to Configure Docebo for Multi-Tenant Architectures

Once upon a time in our bustling and somewhat chaotic office - you know the type, where coffee is the staple and post-it notes stick to everything but the intended surface - Julie and I embarked on a journey. Our mission? Configure Docebo for multi-tenant architectures, which at the time felt kind of like trying to tame a particularly defiant dragon. We were two brave knights - well, enthusiastic coders - armed with laptops and a thirst for adventure. And maybe some spicy chai lattes too.

Now, before getting into our epic saga, let's dive into how you, dear reader, can configure Docebo to master the art of multi-tenancy. If you’ve ever felt lost in the vast forest of technical documentation, fear not. We shall lead the way, not with breadcrumbs, but with a series of steps as illuminating as a GPS on a stormy night.

## Understanding the Needs of Multi-Tenancy

Our first step in configuring Docebo was reminiscent of a late night brainstorming session at the local café. Picture crumpled napkins filled with doodles of complex flowcharts and what looked suspiciously like the beginnings of a Scrabble game. But amidst the chaos, a revelation: each tenant needed their own distinct experience. No shared realms here; only individualized kingdoms. 

In the language of thriving tech ecosystems, multi-tenancy means creating isolated environments for each customer or group which uses the system. With Docebo, this entails setting up different branches (and if you thought real branches were hard to climb, try these virtual ones).

1. **Define Your Tenant Architecture**:
   - Decide how you’ll separate your tenants. Will it be by region? By department? By size of sweet tooth? The choice is yours.
   - Start by mapping out the structure. Sketch it if you must, but make sure it's clear - cleaner than our doodles, at least.

Our whiteboard was a tapestry of boxes and lines, crisscrossing like a game of cat's cradle. Each rectangle a separate entity, brimming with potential. If architecture were art, we had just painted our first masterpiece. Or maybe more accurately, our first draft.

## Setting Up Branches

Oh, branches. Julie and I spent hours configuring these, our faces occasionally pooling perplexion that could rival any soap opera plot twist. But once clarity hit, like a spoonful of icing on the perfect cake, it was bliss. Well, close enough.

2. **Create Branches in Docebo**:
   - **Log into your Docebo** instance (think of this as entering the magical portal to your adventure land).
   - Navigate to `Branch Management` under the `Admin Menu`.
   - Get creative and create a new branch for each tenant according to your predefined architecture.

Picture us, tapping in branch names, imbibing some adventures with titles like “East Division - The Swift Eagles,” and “HR - The Unsung Heroes.” Our strokes on the keyboard were more precise than a maestro conducting a symphony. 

## Configuring User Permissions

There was laughter, there were tears - of joy, mostly, but some frustration snuck in, like an uninvited, but tolerated guest. Configuring user permissions wasn’t just a task; it was an educational journey, a documentary waiting to happen.

3. **Assign Permissions**:
   - Enter the realm of `Advanced Settings`.
   - Head to `Permissions Management`. Here lies the heart of control. Only the worthy may pass, or everyone, depending on your settings.
   - Determine who should have access to what. Managers might get access to reports, learners to courses, and us to more chai lattes.

Remember when Gran used to lock the cookie jar? Well, thankfully Docebo is more generous, though it allows us to determine who gets the cookie. Setting permission levels was akin to ensuring Hogwarts students were sorted correctly into houses.

## Custom Domains and Unique Experiences

A shared address just won’t do; each tenant deserves their own path, like distinct constellations gazing down on us from the night sky, waiting to be named.

4. **Configure Custom Domains**:
   - Leap into `Domain Management`.
   - Set up unique domains for each branch. Forever after, multi-tenancy bliss. 

Envision the moment when we clicked the save button to secure customization. There was an almost ceremonial ring to it - possibly just in our heads - as we celebrated with triumph. Each domain, a new world, a promise that each tenant stands sovereign.

## Testing Your Configuration

Alas, what's a quest without its trials? Testing our setup was much like sneakily sampling Gramps’ pie before dinner, making sure everything fit perfectly.

5. **Thorough Testing**:
   - Create test accounts that funnel through your branches.
   - Simulate real-life usage to check access, visibility, and the all-important, experience.

I remember us, chuckling and chatting, throwing worst-case scenarios at our beautifully crafted configuration, like agile ninjas surmounting invisible barriers. “Julie,” I said, after another round of successful tests, “I think we’ve done it!”

## Refinements and Final Touches

We stayed late at the office that night, like artists perfecting their opus - only, instead of oil paints, we had bytes and branches.

6. **Refinement**:
   - Watch for feedback - gather from users like an endorphin-laden squirrel collects acorns.
   - Adjust the setup based on actual usage and adaptability insights.

Finishing touches are about as joyful as adding whipped cream to a sundae; it polishes off what's already delightful. With our tweaks complete, we both agreed it was time to wrap up, satisfied and perhaps a smidgen proud (though we’d always been taught modesty).

Just as our tale concludes, so does the guide on configuring Docebo for multi-tenant architecture. Together, we've journeyed through the realms of digital alchemy, where every click brought us closer to a final masterpiece. Now, dear reader, it's your turn. Go create wonders in your own configurations and may this guide serve as your faithful companion on the path to success. 

As for Julie and me, cheers to new adventures, and perhaps another pair of spicy chai lattes.