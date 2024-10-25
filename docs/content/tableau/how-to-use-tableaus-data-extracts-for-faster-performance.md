---
slug: how-to-use-tableaus-data-extracts-for-faster-performance
title: How to Use Tableaus Data Extracts for Faster Performance
authors: [undirected]
---


# How to Use Tableau's Data Extracts for Faster Performance

Once upon a time, in a bustling office filled with the quiet hum of machines and the sporadic chatter of caffeinated humans, I found myself wrestling with a beast—no, not literally, but something almost as fierce: a massive Tableau workbook that was taking its sweet time to load. We all know that feeling, right? Standing there, sipping our third cup of coffee, watching the swirling loading icon mock us. But out of the chaos, a revelation emerged like a flash of brilliance: data extracts! And oh, how serene it all became. Let me take you on this journey of exploration, discovery, and much faster Tableau performance.

## The Moment of Enlightenment

The day began ordinary enough, if ordinary meant dodging spreadsheets like laser beams in a spy movie. Julie from accounting waved her hand frantically, trying to catch my attention—her monitor frozen mid-computation. I knew it was time to unleash the magic of data extracts. You see, data extracts in Tableau are like a miraculous blend of a superhero and a magic wand, speeding up performance as if time itself decided to bow to your scripting prowess. 

The solution was both profoundly simple and delightfully powerful: instead of direct connections, we switched to extracts that condensed only the necessary morsels of data. Imagine sipping distilled wisdom instead of chugging from a fire hose. 

### Step 1: Preparing for Data Extraction

Before we perform this formidable transformation, first we need the right ingredients. Think of it as readying your kitchen before baking a cake. Best begin by refining what data you actually need—no more, no less. Connect to your data source as usual, be it SQL Server, Excel, or the mystical realm of Google Sheets. Marie, a curious analyst on our floor, used to say, "Don't bring everything just because you can." Wise words. 

One fine day, I connected to our client-data table—a sprawling affair rivaling a garden labyrinth. From the top menu, select `Data`, then `Convert to Extract`. Bam! The groundwork laid, your masterpiece begins here.

### Step 2: Filtering and Aggregating

Imagine standing before a smorgasbord, deciding which delectable bites make it to your plate. Click on `Extract` in the data source tab. Set your filters like a painter selecting colors—be judicious. Are we interested in only the last fiscal year's data? Perhaps restrict it to a specific department? Apply these filters with gusto.

"Don’t forget aggregation!" chimed in Dave, ever the efficiency crusader, as he walked past, waving a banana. Fetching only the necessary pre-aggregated data makes your extracts nimble, like dancers at their peak.

### Step 3: Data Extraction Time

Now that we've prepared, it's showtime! Click `Extract` and wait—or maybe grab another coffee—but shorter this time. The extract will compress data into an efficient tableau-extract-file with a `.hyper` extension. I remember the first time my extract finished, and the resulting snappiness was a revelation! 

Save this `.hyper` file in a location where you are least likely to interrupt its dance.

### Step 4: Connecting to the Extract

Here's where the magic begins its performance. Open your Tableau workbook or start afresh, and connect directly to your newly minted extract instead of that cumbersome, unruly source. My colleague Wendy referred to it as a delightful shortcut through the matrix. 

Click `Connect to Data`, then `More`. Navigate to your saved `.hyper` file, and link it as if you're establishing a harmonious duet.

### Step 5: Witness the Wonders

Suddenly, our Tableau world became a symphony—I mean, faster, smoother, just better. Visualizations rendered like a swift wind, moving between dashboards felt like swiping through buttered silk. I looked over at Julie, whose monitor glowed with the vibrant speed of fresh calculations, her face lit up in astonishment.

Testing with large datasets now brought joy, not the dread of prolonged coffee breaks or staring contests with a spinning wheel. Yet, there remained the courage to improve. The delight was not just personal but a shared realization, a rare camaraderie birthed from problem-solving.

### Step 6: Refresh and Update

What goes up, as the saying goes, must come down, and in data terms, what becomes static must be refreshed. Periodically, we need to refresh these extracts—especially in the fluid world of analytics. Click `Data`, find your extract source, and choose `Refresh`. Think of it as rejuvenating an old friendship, maintaining the lovely rhythm of your Tableau experiences.

### A Final Thought

Sitting there, as our dashboards glowed with vigor and purpose, it was easy to forget the days of sluggish data slogs. Tableau's data extracts had become more than a tool; they were our trusty steeds, taking us gallantly across uncharted data terrains. Remember though, this power needs respect—update those extracts, keep them relevant, and they'll serve us many an analytical moon.

That day, Julie and I celebrated our newfound efficiency with a quiet tea break—a rare and cherished pause in a world ever hungry for speed and data. And so, dear friends, go forth armed with this wisdom, embracing the wondrous world of Tableau data extracts, where performance issues fade away like distant echoes, leaving you with naught but satisfaction and swift execution.