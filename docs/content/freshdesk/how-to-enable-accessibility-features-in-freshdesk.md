---
slug: how-to-enable-accessibility-features-in-freshdesk
title: How to Enable Accessibility Features in Freshdesk
authors: [undirected]
---


# How to Enable Accessibility Features in Freshdesk: A Journey of Inclusivity

Ah, accessibility. It’s like learning to ride a unicycle. Difficult at first, but once you get it, everything changes. I remember the day vividly. Janet from accounting, bless her heart, asked me if Freshdesk supported screen readers. I paused - bless my own heart - having never thought about it, not once. Suddenly, a light bulb. A eureka moment. And that’s where our story begins because just like Janet needed answers, we all need a bit of enlightenment sometimes.

So here we are on this delightful escapade through the labyrinth of Freshdesk, where we will demystify the process of enabling accessibility features - without any unnecessary jargon. Trust me, if I can do it, so can you.

## Unraveling the Mystery of Accessibility
Let's take a moment to appreciate how technology can truly bridge gaps. On our quest, we realized how crucial it is for software to be inclusive. But hey, software won’t change by wishful thinking alone. That’s what we’re here for — action. Janet and I rolled up our metaphorical sleeves and delved into the Freshdesk waters.

### Step 1: Understanding the Accessibility Feature Requirements
Imagine the scene: Janet with her legal pads, me with my laptop — both ready for the great mission. The first step is knowing what you need. Different folks have different strokes, right? Screen readers, keyboard navigation, high contrast themes; it’s all about options.

Here's what you can focus on:
- **Screen Reader Support**: Make sure text elements are recognized by popular screen readers like JAWS or NVDA.
- **Keyboard Navigation**: All interactive widgets should be accessible via keyboard.
- **Color Contrast**: Ensure content is visible without eyestrain.

### Step 2: Configuring Basic Settings in Freshdesk
Janet is a trooper, and she gamely started with the basics. Freshdesk offers in-built support for accessibility, but you need to know where to find it. Imagine hunting for hidden treasure — it's there, you just need the map.

1. **Log in to Freshdesk:** The basics! Username. Password. Voilà.
2. **Navigate to Admin Panel**: Most things hide here. Think of it as the control room of the spaceship.
3. **Select Accessibility Settings**: Look for accessibility or related options. It's like peeking into the refrigerator for a midnight snack.

### Step 3: Enabling Screen Reader Compatibility
Janet, with her delightful penmanship, took notes like a pro. Making Freshdesk screen reader friendly involves making sure all elements are "seen" by the software.

1. **Use ARIA Labels**: Ensure all interactive elements have ARIA labels for better interpretation by screen readers. It’s like putting up signposts on a hiking trail.
   ```html
   <button aria-label="Submit Ticket">Submit</button>
   ```
2. **Semantic HTML**: Keep the HTML clean and tidy. Your screen reader will thank you.
   ```html
   <header>Accessibility Settings</header>
   ```

### Step 4: Implementing Keyboard Navigation
The keyboard is a mighty tool, so we dived into this aspect next. Janet is a wizard with shortcuts, so this was her jam. People should navigate Freshdesk without a mouse.

Here's how you do it:
- **Tab Indexing**: Make sure the tab order is logical. It’s like lining up dominos.
   ```html
   <input type="text" tabindex="1">
   <button tabindex="2">Next</button>
   ```
- **Focus Management**: Give visual cues when an element is focused.

### Step 5: Adjusting for High Contrast Mode
Think of this as adding flavor to a dish. If you're stirring the pot (or adjusting contrast), you want people to *see* what's possible.

- **Custom Themes**: Freshdesk offers themes that can be adjusted for contrast.
  - Go to Settings → Themes, tweak the CSS for better visibility.
  ```css
  body {
    background-color: #000;
    color: #fff;
  }
  ```

### Step 6: Testing the Waters
For a task like this, we became testers. We were like kids with a new toy. Testing is fun, and also important to understand the user experience.

- **Run Accessibility Audits**: Use tools like WAVE or Lighthouse to get insights.
- **User Testing**: Gather feedback from real users who need accessibility features.

### Step 7: Continuous Improvement
We learned that this is not a one-time setup but a journey. There is always room to improve. Janet and I made a pact to revisit our settings periodically.

- **Feedback Loop**: Encourage users to provide feedback.
- **Stay Updated**: Keep pace with new tools or updates in accessibility standards.

## Wrapping Up Our Adventure
Enabling accessibility in Freshdesk isn’t as tricky as it sounds. It’s all about being aware and making small, incremental changes that can have a profound impact. Janet was thrilled - and I was proud - because, together, we made a little corner of the digital world better.

So, why not take the plunge? Enlighten your Freshdesk, and let's make tech work for everyone. It’s a journey that starts with a single step - and let’s be honest - why shouldn’t it be a warm, fuzzy, inclusive step?

And as we stand here, reflecting on this escapade, let’s commit to more inclusivity and kindness in our digital and real-world communities. For everyone. Always.