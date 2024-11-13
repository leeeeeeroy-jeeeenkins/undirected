---
slug: how-to-set-up-customer-training-portals-in-docebo
title: How to Set Up Customer Training Portals in Docebo
authors: [undirected]
---


# How to Set Up Customer Training Portals in Docebo

There’s a kind of magic in watching a process unfold in real-time, much like when we figured out how to set up our first customer training portal on Docebo. It was a sunny morning, the kind of day where the world seems to hum with possibilities. I had just made myself a steaming cup of coffee, the aroma swirling around me like an old friend. We sat down in front of the computer with a mission: to conquer the world of e-learning—or at least set up a customer training portal that didn’t make us both want to scream into a pillow.

## A Glance at Docebo’s Playground

Docebo is like the cool kid on the block of Learning Management Systems (LMS), oozing swagger and a little bit of mystery. Initially, we looked at each other and thought: How tricky could it be? Spoiler alert: At first, it felt as if we had jumped into a swimming pool without floaties. Yet, here is where the nuts and bolts of setting up a customer training portal unveiled themselves. Our first challenge, or maybe it was a puzzle, was logging into our Docebo account. Those usernames and passwords—guardians at the gate—seemed more daunting than a dragon watching over its hoard. Don’t even get me started on two-step verification. 

```bash
# Log into your Docebo account
username: your-email@yourcompany.com
password: yourPassword123!
```

## Creating the Portal: Not as Scary as Naming a Dragon

After a deep dive through cyber space, we landed on the dashboard, a vast terrain ready to be molded. The first step was creating our training portal. We found the settings icon—small, yet mighty, sitting there like some kind of ‘portal’ middle manager—and clicked on it with all the power two index fingers could muster. If the computer screen happened to be a sheet of glass, it may very well have cracked under the pressure.

Under **Platform Configuration**, there it was: the **Domains & URLs** tab. Click it and bam—you’re directed to a page where dreams of customer training portals with engaging content and world peace could begin. Imagining the faces of our future learners, noses pressed against the screen with wonder, I smiled. 

### Setting Up the Environment

It was time to dress up our new portal. Picture a curtain being drawn back for the first act of a play.

1. **Primary Domain**: Enter the primary domain name. You've thought about it all night, maybe even dreamt about it—now it's time to type it, warmly and confidently like you would your name or perhaps your favorite dessert.

   ```bash
   # Setting Primary Domain
   primaryDomain: portal.myawesomebrand.com
   ```

2. **Additional Domains**: Define other domains if your portal is going to wear different hats. Who said a brand can’t have multiple personalities?

3. **Branding**: Customize your portal’s look. Here is where art meets function. We tinkered with logos, colors, and, yes, even the beloved font choices. I couldn’t help but reminisce about a childhood memory of picking out new crayons every school year. You could almost smell the fresh wax as we played with Docebo’s branding options.

## Enroll Learners: Inviting Folks to the Party

With our portal taking shape, the next chapter led us to the whistle-blowing, flag-waving, casual invitation process—inviting learners. Some say sending an invite feels like sending out a wedding invitation. Entering the **Users** tab from the main menu, we found ourselves staring at a bewildering list—empty, but hauntingly full of potential.

Adding users was as simple as aligning a row of dominoes. If only pressing a **+** was always this satisfying.

1. **Add Users**: Manually or via CSV import if you’re feeling extravagant and dealing with entire kingdoms of learners.

   ```csv
   username,email,first_name,last_name,role
   jdoe,jdoe@company.com,John,Doe,learner
   ```

2. **User Fields**: Define any custom fields to capture all those delightful details about your new friends.

3. **Learning Plans**: Assign a plan or courses tailored to each user's needs. It was like weaving a personalized tapestry; everyone gets a different color, yet they’re part of a bigger picture. 

## Crafting the Content: Oh, the Creativity!

What’s a training portal without content, right? It's like a cake without icing or a spaceship without an engine. We sauntered over to the **Courses** section and paused, realizing this was a massive opportunity to create real, impactful learning experiences.

Setting up a course felt like baking—a pinch of this, a dash of that, all culminating in something warm and inviting.

1. **Add a Course**: Name it something that would make even your high school English teacher weep with pride.

2. **Modules**: Here is where your creativity gets to run wild. Upload files, link to videos, create webinars, or yes, those dreamy SCORM packages.

   ```bash
   # Sample SCORM package upload
   scormPackage: './path/to/your/course.zip'
   ```

3. **Course Properties**: Assign purposes to the content, determine the assessment methods, and wrap it all up with a shiny bow of prerequisites. 

## Automate and Optimize: The Magic Continues

After the content was sizzling in the digital oven, the not-so-secret elephant in the room was using automations. A fancy word for making sure everything ticks along without micro-managing like a helicopter parent.

1. **Automation App**: Enabled smoothly through the **Apps & Features** area.

2. **Configure Automations**: Think of this as backstage crew: create rules for notifications, course enrollments, and reporting. Automations are an unsung hero—like cleaning your kitchen while you sleep.

3. **Reports and Dashboards**: Like peering into a crystal ball but techie-style. Customize how data reports back to you while sipping on an espresso or herbal tea. 

## Reflecting on the Journey

By this stage, we'd woven together a training portal that was not just functional but a joy to navigate. It felt like a garden—endlessly growing and evolving, lovingly tended—we could almost hear the rustling of knowledge sprouting in every corner. 

Setting up a customer training portal in Docebo had facets of a grand adventure: dragons were definitely tamed, and new lands were charted. As we leaned back, the computer humming a lullaby, coffee mugs now empty, it was clear that this journey, geeky as it was, had brought us—and our learners—somewhere new and wonderful.

And isn't that what any great story aims to achieve?