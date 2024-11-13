---
slug: how-to-customize-the-docebo-ui-for-branding-purposes
title: How to Customize the Docebo UI for Branding Purposes
authors: [undirected]
---


# How to Customize the Docebo UI for Branding Purposes

## A Humble Beginning

Once upon a time—not so far away, in fact, but precise enough to be last Tuesday—I found myself ensconced in the cozy embrace of a freshly brewed cup of coffee. Isn't it funny how these moments of caffeinated bliss can morph into transformative epiphanies? There I sat, fingers poised above the keyboard, pondering the ever-elusive question: How does one make the digital learning space reflect the spirit of our brand, not just merely a vessel for mundane information?

We were using Docebo for our LMS (Learning Management System), and the haunting whispers of branding dreams danced in the periphery of my mind—do you feel that too? It was time to customize. As the warm steam curled from my cup, I realized the interface might as well have been wearing a neon sign screaming "Generic!" But no more. Let's dive into the labyrinth and emerge with something more…us.

## Embarking on the UI Customization Odyssey

Imagine, if you will, our hero (that's collectively us, dear readers) beginning this journey at the Docebo dashboard. We had weapons of choice: a mouse in one hand, a vision in the other. We would need them both.

### Step 1: Setting the Stage with Admin Powers

First thing's first, channel your inner superhero. Activate, channel, and assume the role of an *Admin*. Without these credentials, well, it’s like trying to climb Everest in flip-flops—ill-advised and slightly doomed.

1. **Log into Docebo**: The gateway to our transformation. I often pause here to admire—if only for a fleeting moment—the serene chaos of all that needs changing.
   
2. **Access the Admin Menu**: Gently click on the gears icon, aptly representing settings. Now, navigate to the part labeled **“Branding and Look & Feel.”** Feel the power surging through your fingertips.

### Step 2: Dancing with Logos and Colors

With the fervor of a thousand artists, now's our chance to replace the default logo that's likely blander than overcooked rice. 

1. **Upload Your Logo**: Hit the “Upload” button next to the Logo field. Select a file, and voilà! Your logo graces the top left of the interface, like a dignified monarch surveying their realm.

2. **Select the Colors**: Here’s where it gets personal. Under the “Colors” section, rethink, recall, remember how your brand’s colors may influence moods—our very own emotional puppeteers.

   ```yaml
   # Sample theme color configuration
   primary_color: #0056b3
   secondary_color: #f1f1f1
   text_color: #333333
   ```

While adjusting colors, I remember the time Jane from marketing got so entranced by our new palette she equated them to summer skies and winter warmth—such poetic musings. But oh, what a difference a color makes!

### Step 3: Crafting a Mystical Home Page

Now, challenge the status quo of clunky dashboards and unimaginative layouts. Let us not settle!

1. **Home Page Customization**: Navigate back to the Admin Menu and find "Homepage Configuration". It almost feels like redecorating a beloved room in one's home.

2. **Widgets Dance**: Add, remove, and rearrange widgets. Here, introspective nuances become tangible features. Did you know you can customize HTML Widgets? Perfect for bespoke messaging or announcements—we once embedded a “Quote of the Day” feature to inspire a sense of whimsy.

   ```html
   <div class="quote-widget">
       <h3>Quote of the Day</h3>
       <p>"The only limit to our realization of tomorrow is our doubts of today." – Franklin D. Roosevelt</p>
   </div>
   ```

### Step 4: Fonts and Typography, the Unseen Voice

Fonts are like the unsung heroes of design—trust me. The choice goes beyond aesthetics; it's a silent narrator guiding the learner through terrains of information.

In the Admin Menu, select “Theme” and venture into typography. Choose fonts that sing to your brand's essence. We once opted for something bold and unconventional—because sometimes, we dare to be different.

## Onward to Personalization

Now, at a glance, do we see how our online educational fortress stands resplendent? Not yet? Fear not. Remember the time we added custom CSS? Dream big, I say. Let’s make it personal.

### Step 5: Diving into Custom CSS

For those among us with a penchant for tinkering—a calling, if you will—custom CSS is the canvas upon which you can paint your masterpiece.

From Admin Menu, go to “Advanced Settings” and select “Custom Styles”. Here's where the magic whispers its secrets.

```css
/* Custom Style Example */
body {
  background-color: #f5f8fa;
}

.header {
  padding: 20px;
  background-color: #123456;
}
```

It brings tears—or was it the paint fumes? Either way, CSS is where you craft those quirks that make the interface sparkle.

### Step 6: The Test of Trials

Before the curtain falls and applause erupts, we must test and re-test—like ancient alchemists enduring trial and error. Check the interface across countless devices, screens, and all that exists in between.

I recall an evening of testing where half the team simulated different environments from smartphones to fridges (smart fridges are indeed involved in everything these days), each singling out any quirks or anomalies crying for attention.

## The Grand Finale

At the cusp of the culmination, it's a cosmic sense of unity and satisfaction. Do well to remember: customization is an evolution, not a destination. Reflecting our brand in such a digital realm is an ongoing saga—spare no room for complacency.

As we lean back in our chairs, contemplating the journey—a triumph indeed—a final sip of that long-forgotten cup of coffee accompanies our cherished works. Now, go forth and show the world (or at least your team) what the power of branding can truly do within the confines of Docebo. Bravo, we did it.

---

In the sweetness of inspiring moments and caffeine highs, here's to designing not just systems, but experiences. Let these words be your guide as you carve a path beholden to creativity, joy, and a little bit of irreverence sprinkled like so much digital fairy dust.