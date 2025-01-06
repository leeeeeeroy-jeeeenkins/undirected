---
slug: creating-mobile-friendly-dashboards-in-qlikview
title: Creating Mobile Friendly Dashboards in QlikView
authors: [undirected]
---


# Creating Mobile Friendly Dashboards in QlikView

We've all had those days when technology just doesn’t want to play nice. It was one of those crisp Tuesday mornings, you know, the kind where the coffee is just a tad too hot and the world seems draped in a soft grey blanket. I found myself elbow-deep, metaphorically, in a massive QlikView project, only to realize that my beautiful desktop masterpiece transformed into a Frankenstein's monster when viewed on mobile devices. The elegant charts resembled squashed bugs; text was microscopic, and the overall user experience hinted something invented in a parallel dimension where usability doesn't exist.

But rather than curse the gods of poor digital design — though I admit, I may have grumbled at them a tad — this led us to an unexpected quest. Our destination? Crafting mobile-friendly dashboards in QlikView, our trusty data visualization tool. Grab a chair, your favorite mug of something lovely, and let’s unpack this adventure together.

---

### The Epiphany Moment: Understanding Mobile Constraints

Marie — bless her heart — was the unfortunate soul to get the first sneak peek of my mobile disaster. Her puzzled expression was monumental. Much like watching a mime perform at hyper-speed, it spoke volumes without sound. This situation demanded we start by understanding our limitations. Here’s what we learned.

**Screen Size Woes:** Mobile screens are not forgiving. They're like a teenage diary, small and filled with mysteries you have to squint at to understand. In this world, less is more. And by less, we mean streamlined, concise data for speedy insights.

**Finger Friendly Elements:** Let’s face it; our fingers are not precision instruments. Like dropping a loaded spoon, they can’t navigate tight spaces without making a mess. Buttons and text items need to be spaced generously so that tapping doesn’t resemble playing a game of whack-a-mole.

With our constraints pocketed, it was time to reimagine our dashboard design for smaller screens. There’s a certain joy in taking something complex and making it feel seamless. Like fitting a grand piano in a mini cooper.

### Navigating the Interface: A Framework for Mobile Mastery

Our next step was to sketch a blueprint — a roadmap, if you will — for how this transition to mobile might look, and who knows more about trials and plans than our old windsurfing buddy, Dave? Dave had a saying: "Without a clear path, you'll end up swimming more than surfing." A mantra we took to heart.

**1. Simplicity is a Virtue:** Start clean. Select widgets that tell your story without overwhelming the canvas. Remember those timeshare presentations that stretch too long? Let’s not repeat that.

**2. Locate Your Priorities:** Place vital info where it’s most accessible. In mobile terms, "above the fold" is prime real estate. Your data should jump out, not hide in some forgotten corner like unwanted broccoli on a dinner plate.

**3. Test, Test, and Then Break It:** Possibly the most crucial step. We need to see this dashboard fail to adapt. Marie’s expression was gold; our trial by fire was watching her interact with our test app, hunting down snags like Sherlock Holmes in a digital realm.

```qlikview
SET vResponsiveMode = 1;

SUB SafariCompatMode
    'Adapting settings for different browsers
    IF Browser() = "Safari" THEN
        vResponsiveMode = 1; 'Enabling modes specific to Safari
    END IF
END SUB
```

### The Tools in Our Toolkit: Adapting QlikView’s Features for Mobile

Once upon a time, I fancied myself a semi-pro at understanding QlikView’s nuanced features. Then the mobile conversion came along, and we dove into settings most users rarely encounter. Let's talk tools.

**Responsive Faces:** QlikView allows for conditional show/hide properties. A wonderland feature for selectively displaying elements based on device type. Think of it as wardrobe choices — sometimes you’re in flip-flops, sometimes in brogues, but never both.

**Expression Traps:** Set your visualizations to adjust dynamically. This is where we craft queries that flex their content based on screed width. Yes, like magic layers of a cake, hidden until you slice into it.

```qlikview
CHART
IF (ScreenWidth() < 768, 'Mobile View', 'Desktop View')
'...
```

### Rolling It Out: User Testing and Continuous Feedback

Finally, with a spring in our step, the creation was ready to face the real world. Real users navigating real scenarios. Here lies the true test of all creative endeavors; will it fly, or will it flop?

**Embrace Imperfection:** If our initial mobile-friendly dashboard was the peak of innovation, then unicorns were real, and everyone had a Tesla. It wasn't perfect. But what it was—a step forward.

**Iterative Improvements:** Each piece of feedback we received was like a breadcrumb on a trail — little by little leading us to a transformed final product. And remember Dave? He always said, "The best surfers are actually adept swimmers." So we swam through feedback, learning and evolving.

### Painting the Final Picture: Reflections on the Mobile Dashboard Journey

Now the dashboard sings its mobile-friendly tune like a young rock band that just found its rhythm. And while the road was bumpy — we may have hit a pothole or twenty — the outcome was worth the ride. 

So here we are, with better dashboards and a deeper understanding of QlikView’s vast potential. It was a group journey, defined by unexpected challenges and abundant learning. And at each stumble, we had Marie’s laugh and Dave’s philosophy to remind us that we're all in this together, navigating new experiences with curiosity and creativity at the helm. 

Tackle your mobile dashboard challenges with gusto, humor, and patience. And always, always leave room for iteration. After all, even the best surfers once had to learn to simply float.

`//Thanks for riding along!`