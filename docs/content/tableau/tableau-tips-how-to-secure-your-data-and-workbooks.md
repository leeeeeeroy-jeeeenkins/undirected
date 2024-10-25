---
slug: tableau-tips-how-to-secure-your-data-and-workbooks
title: Tableau Tips How to Secure Your Data and Workbooks
authors: [undirected]
---


# Tableau Tips: How to Secure Your Data and Workbooks

In the summer of '21, I found myself sprawled across a faded floral couch in Aunt Matilda's living room. Sweat glistened on our brows as the overhead fan lazily stirred the hot air. Aunt Matilda, armed with her ancient laptop, had been trying desperately to open a Tableau workbook sent by her knitting buddy, Doris. You see, the issue at hand was that Doris had accidentally shared the workbook with the world—data and all—with one misstep. This incident, although seemingly benign, set off a chain reaction of chaos among the knitters, each concerned about privacy. It became a tale of caution in our little family, and from that day forward, data security in Tableau was forever etched into my consciousness.

**Subsection 1: Understanding the Importance of Data Security**

Under the watchful eye of Aunt Matilda—I can still hear her voice quavering with suspense—our first mission was understanding why data security was not just another tedious checklist item, but a vital component of working with Tableau. Now, unlike Matilda, who had only ever used her computer to find elusive knitting patterns, we grasped why safeguarding this digital beast was crucial.

Data security prevents unauthorized access and leaks—a painful lesson Aunt Matilda and I learned the hard way. Ensuring proper permissions and controls can make the difference between a trusted report and one causing mass hysteria at your local knitting club. Just the thought leaves me with a slight shudder.

**Subsection 2: The Dance of Permissions**

Now, let's dive into the nitty-gritty—grant access wisely. Picture Aunt Matilda pirouetting as she discovered how to manage permissions (a preposterous image, truly). But the adventure of discovering Tableau Server’s permission settings was akin to a grand ballroom dance. Graceful, deliberate, and if done wrong, prone to stepping on toes.

Here's how we do it: 

1. **User Roles** - Determine the role each user needs. Are they mere mortals—viewers? Or perhaps, mighty creators? Decide who gets to play DJ and who just listens to the tunes.

2. **Project Level Permissions** - This is where the magic happens (cue jazz hands). Choose who can access which project. You wouldn't give a puppy the keys to your Porsche, would you? Exactly.

3. **Workbook & Data Source Permissions** - Aunt Matilda would nod in fierce agreement here. Ensure roles reflect the power each individual holds. Can they modify, save, or merely peek? Decisions, decisions!

4. **Testing Permissions** - Once our dance steps were refined, it was time to take them for a spin. Practice makes perfect—ensure everything works as intended. 

```plaintext
// Practice Test
// Ensure users only have access to the intended sections.

if(thisUser.role === 'viewer'){
  grantViewAccess(workbook);
} else if(thisUser.role === 'editor'){
  grantEditAccess(workbook);
}
```

**Subsection 3: Securing Data Sources**

The heart of the Tableau ecosystem—data sources. Aunt Matilda, bless her heart, likened this to safeguarding her secret chocolate chip cookie recipe. The parallels are uncanny—both are precious, revered, and potentially dangerous in the wrong hands.

1. **Authentication** - Choose wisely between database, prompt, and stored. Aunt Matilda once stored her password on a post-it note—don't do that.

2. **Data Extracts** - If you're using extracts (and you probably are), remember they're like little treasure chests. Set up encryption for developed secrets; don't leave them unprotected.

3. **Embed Credentials or Not** - This choice haunted Aunt Matilda for weeks, but eventually, she understood. Only embed when absolutely necessary, it's like lending out your most comfy slippers—do it sparingly.

**Subsection 4: Publishing Workbooks—The Safe Way**

Publishing in Tableau, as Aunt Matilda often murmured, is both an art and a science. The canvas? Your workbook. Your tools? Patience and precision. Publishing securely to Tableau Server or Online helps maintain the peace—necessary for a smooth, yarn-filled day.

1. **Lock Your Door** - Or, set view permissions before publishing. Aunt Matilda's neighbor, Gerald, will not appreciate stumbling onto your ROI dashboard by mistake.

2. **Manage Data Sources** - Beware of embedded data sources becoming tangled—it happens. Ensure data sources are independently managed and permissioned properly.

3. **Incremental Refresh** - Not just a fancy term—use it when publishing large workbooks. Trust us, it's a life-saver—right, Aunt Matilda?

4. **Version Control** - A repeatedly worn phrase by Aunt Matilda. Maintain version control. Always. No exceptions. Use descriptive names and organize versions sensibly.

**Subsection 5: Additional Layers of Security**

Finally, we add some extra snuggly blankets of security. Because, much like Aunt Matilda on a winter’s night, one can never have too many layers of protection.

1. **SSO and MFA** - Single Sign-On and Multi-Factor Authentication. They sound like tech jargon, but picture walking through a door that only recognizes you when you also enter your secret song—secure and chic.

2. **Data Masking** - A must if Aunt Matilda's strategic eyes are watching. Mask sensitive fields to conceal their true nature—true wizardry!

3. **Audit Trails** - Establish audit trails to identify curious fingers or malicious intent. Trust us, nothing escapes Aunt Matilda’s scrutiny.

4. **Training and Communication** - Share knowledge. Have a tea party—Aunt Matilda's suggestion—and exchange insights on data security, making it part of your culture.

In Aunt Matilda’s living room, surrounded by yarn and cookies—safe now, thanks to our efforts—our minds brimmed with newfound security insights. As we basked in the glow of her everlasting gratitude, it became clear: securing data and workbooks in Tableau isn't just preventing mishaps; it's about dignity, trust, and keeping the tranquility alive. Hopefully, these pointers illuminate your path as you sashay confidently through the tableau of data security—one shifty glance at a time.