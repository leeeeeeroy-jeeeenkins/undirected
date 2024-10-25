---
slug: how-to-share-and-publish-tableau-workbooks-on-tableau-server
title: How to Share and Publish Tableau Workbooks on Tableau Server
authors: [undirected]
---


# How to Share and Publish Tableau Workbooks on Tableau Server

### Our Tableau Journey: A Tale of Two Data Enthusiasts

Once upon a random Tuesday, Carina and I found ourselves knee-deep in a data blizzard: rows and columns sprawled like an unruly tapestry across our very own Tableau playground. This was not a lazy afternoon’s dalliance with data; oh no, this was our magnum opus—looming deadlines, caffeine-induced jitters, and a hope as audacious as trying to change the Wi-Fi password without locking everyone out. The simple beauty of it all was overshadowed by a mighty question: How do we share this glorious bundle of insights with the world, or at least with Bob from marketing? That dilemma nudged us into the mystical realm of Tableau Server, where we learned—through trial, error, and bursts of pure, unadulterated discovery—how to elegantly share and publish our workbooks.

### Setting the Stage: Tableau Server at First Glance

And so, wide-eyed and slightly perplexed, we reached the threshold of Tableau Server—a bit like gazing at a cake and knowing there’s a way to eat it neatly, without making a mess of yourself in a room full of people. The options seemed both straightforward and a tad obfuscating at the same time. “Let’s do this,” Carina declared, her voice echoing with the confidence of someone who reads the IKEA manual only after assembling.

First things first, you *gotta* be connected to the Tableau Server. Just like trying to sync our moons between devices, first ensure you've got your server URL and login credentials at the ready. It's like knowing the right password to a secret club, essential but—let's be honest—tedious.

**Step 1: Connect to Tableau Server**

1. Launch your Tableau Desktop.
2. Navigate to `Server` on the top menu.
3. Choose `Sign In` from the dropdown.
4. Enter your Tableau Server URL and hit enter.
5. You'll be greeted by the login page. Input your credentials, breathe, and click `Sign In`.

Huzzah! Welcome to the digital clubhouse. Carina let out a cheer that almost startled the cat.

### Crafting the Tale: Workbook Prep for the Audience

Here’s where things took a creative turn. Our data story—housewarming sales trends, employee caffeine consumption (yes, again), and the fascinating correlation between the two—deserved a smooth narrative arc, right from our Tableau Desktop heroes to the sprawling realm of Tableau Server.

**Step 2: Ready Your Workbook**

Before publishing, ensure your workbook is as polished as your grandma’s silverware—put those storytelling elements in place, fine-tune your dashboards, double-check filters and parameters, and save! Hit that save button like it owes you money.

**Step 3: Fine-Tune Permissions and Settings**

As we’ve learned through a spaghetti incident of access issues, knowing *who* gets to see *what* is crucial. Tableau Server loves its permissions like a bouncer loves a guest list. You don't want Bob seeing the secret sales strategy chart before the big meeting, do you?

- Set permissions wisely. Right-click your workbook, select `Permissions`, and ensure each colleague doesn’t have more access than necessary.
- For specific folk, like Dave in finance who travels with a trusty old spreadsheet, give additional privileges if they must interact with data instead of just viewing.

### Publishing the Masterpiece: The Joy of Clicking ‘Publish’

Publishing, oh the sheer excitement—or existential dread—of clicking that button! It was around this time Carina brought out a victory coffee. Publishing the workbook is like getting the final draft out—both terrifying and exhilarating.

**Step 4: How to Publish Your Workbook**

1. In Tableau Desktop, go to `Server` > `Publish Workbook`.
2. Choose the Tableau Server you’re connected to.
3. A publishing wizard pops up, much less mystical than it sounds, for which you must thank someone.
4. Here, pick a project—think of it as your workbook’s new digital home.

- **Name it Thoughtfully:** A title that speaks to the workbook's true essence, something like "Sales Enchantment 2023" or whatever rings your bells.
- **Details Matter:** Describe your workbook, like you’re selling a painting, only with less paint and more data.
- **Permissions Again:** This screen lets you confirm permissions. Adjust them—linger if you must. This isn’t a one-time door, permissions can be modified later but get them right the first time.

5. Hit `Publish`, then dance a little—it’s done.

### After Publishing: Life Beyond the Server

We had imagined it ending there with a triumphant high-five, but dear reader, there’s life beyond the ‘Publish’ button. Publishing isn't the end of our journey; it's another chapter—a revelation.

**Step 5: Share Your Workbook**

Tableau Server invites sharing.

- To share with a link, navigate to the workbook in Tableau Server, simply copy the URL, and distribute like memes in a workplace chat.
- For a broader audience, explore embedding your visualizations into blogs or websites through the `Embed Code` option. Code blocks are tremendous: 
```html
<iframe src="your-tableau-url" width="800" height="600" frameborder="0"></iframe>
```
AND for Julie back in sales, customize sharing for her favorite cloud service, just to watch her genuine surprise.

### Celebrate the Connection: Beyond Technicalities

Publishing in Tableau is like crafting the ultimate mixtape. It’s a celebration of knowledge—one that, hopefully, gets its intended audience dancing to the beats of data-driven insights. And let us tell you, the real joy is in seeing your team navigate, explore, and *interact* with the stories you stitch together. 

Our Tuesday culminated in smiles, victory sips, and a dash of office glory. After all, isn’t that what sharing insight is about? Connecting dots and people, like a data whisperer—or an accidental tech genius on a quest for knowledge.

This little escapade in the world of Tableau Server taught us: it’s not just about hitting 'Publish'; it’s about unleashing the potential to spark decisions, to illuminate paths, and just maybe, to make Bob from marketing finally utter something worthy in the team meeting.

Here’s to the dance of data and the art of sharing it—one tableau at a time. Cheers, dear data travelers, until our next itinerant pursuit of the infinite world of visual storytelling.