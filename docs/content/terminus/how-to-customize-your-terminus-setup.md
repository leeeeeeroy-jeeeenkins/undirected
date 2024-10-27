---
slug: how-to-customize-your-terminus-setup
title: How to Customize Your Terminus Setup
authors: [undirected]
---


# How to Customize Your Terminus Setup

I remember sitting in my dimly-lit study, surrounded by a pandemic-induced mountain of coffee mugs and books I meant to read. I was on a quest—a very personal quest—to transform the drably utilitarian look of my Terminus setup into something truly magnificent. You see, I yearned for a digital workspace that resonated with my taste, the way a perfectly seasoned bowl of ramen hits the soul on a snowy evening. Let’s embark on this journey together, shedding the mundane one tweak at a time. 

## The Awakening

The urge to rearrange one's digital environment often strikes unexpectedly, not unlike a neighbor’s cat sauntering into your home uninvited. Perhaps it was an old friend, Greg, describing how he made his setup blindingly terrifying yet efficiently crisp, that nudged me into this rabbit hole of customization—a place where code meets art. As he demoed his snappy animations and personalized hotkeys, I realized this was indeed possible for us all.

Before diving in, install Terminus from [the GitHub repository](https://github.com/Eugeny/terminus), unless you already don't remember when you did. Let’s proceed. 

## Let There Be Themes

Changing your theme is like putting on a new outfit; it sets the mood for your hacking hijinks. The first task in our digital makeover? Spicing up the interface with a variety of colors and themes jerking us out of the banality with every launch.

To change your theme, navigate to the 'Settings' tab. It's like adjusting your sails to catch a fresh breeze. Go to 'Appearance.' Here, we're blessed with delightful choices. Each one resembles trying on a new persona without the bothersome need for new clothes. Select a pre-installed theme or, if you fancy a unique design—download from online repositories.

```json
{
  "theme": "dracula-pro",
  "font": "Fira Code Retina",
  "fontSize": 14
}
```

Applying a theme is like finding a song that stirs your soul, but this tune lives in pixels.

## Font-astic Adventures 

Ah, the font! We underestimate its power—don’t. A font reflects our innermost aesthetic sensibility, much like the choice between tea and coffee. Trust me, my world changed when I beheld a command line decked out in 'Fira Code.' Greg swore by his slick monospace style, which made his lines of code rival the beauty of modern art.

Here's how you can experiment with fonts until you find your bliss:

1. In 'Settings', click 'Appearance'.
2. Find 'Font'.
3. Try different fonts—pre-loaded ones or venture to download new ones.

For a sublime start, here's my favorite’s snippet:

```json
"fonts": {
  "default": "Fira Code",
  "fontSize": 16
}
```

Finding the right font is akin to discovering your new favorite book—transformative and deeply personal.

## Keybindings of Power

One evening, Greg, with smug satisfaction, demonstrated how he rebounded through his tasks using custom hotkeys. To say it was inspiring would be like saying the sun is warm. Customizing keybindings is our spellbook of shortcuts; casting magic with a mere tap.

To create or modify these keybindings:

1. Open the 'Settings' menu.
2. Select 'Hotkeys'—therein lies your secret arsenal.
3. Add or edit bindings as you prefer.

Feel free to use the example below to begin your journey:

```json
"hotkeys": {
  "openNewTab": "Ctrl+T",
  "closeTab": "Ctrl+W"
}
```

We become maestros in our virtual symphony, orchestrating with elegance and efficiency.

## Window of Opportunity

Positioning your Terminus window is strategic, not unlike arranging furniture in a feng shui-pleasing manner. Greg, during an unforgettable LAN party—full of nostalgia and pizza—propped his window so perfectly on his ultrawide screen that I could feel the harmony radiate.

We can do the same by tweaking window settings for optimal comfort. In settings, under 'Window', adjust parameters like size, position, and whether you want a frame—like so:

```json
"window": {
  "width": 800,
  "height": 600,
  "frame": false
}
```

Finding the right window setup is finding where flow meets form.

## Plugins: The Secret Sauce

Next, plugins, dear comrades. Discovering these felt like unearthing treasure in a field of daisies. They elevate the basic into excellence, walloping on features Terminus doesn’t natively include—yet needs.

1. Head to the 'Plugins' tab.
2. Browse through the plugin repository.
3. Install and configure according to your heart's desire.

One sublime recommendation is the 'Terminus Git' plugin, essential for smoothing Git workflows. Installation resembles this:

```shell
plugins install terminus-git
```

Using plugins is like having a bespoke coat stitched to fit just you.

## Embrace Your Setup

There was a unique delight when Greg and I stood back, gazing at our newly customized Terminus setups, transformed right before our eyes, not needing approval from the gods of the bland and uninspired. It was an artistic triumph, one unparalleled in its tailored utility and aesthetic pleasure.

Revel in each choice, each trial and err—each time you've reshaped space in your digital realm. After all, this is your world and your masterpiece.

So, as we sign off from this adventure, may your adjusted Terminus glow with both the nostalgia of Greg's random LAN party triumphs and the sophistication of cherry-picked fonts and hues. Smile at its sight every morning. It’s like being greeted by an old friend enlighten with fresh garb—a reminder we can customize our chaos, one line of code at a time.