---
slug: setting-up-drift-for-e-commerce-sites
title: Setting Up Drift for E Commerce Sites
authors: [undirected]
---


# Setting Up Drift for E-Commerce Sites

So there we were, tangled in the digital jungle of online shopping, clutching our laptops like adventurers gripping a compass. It was a Tuesday afternoon, one of those days where grey skies embrace the town. Our mission? To set up Drift on our fledging e-commerce site—certainly a task we'd optimistically believed would be a mere walk in a virtual park. Every click felt like a leap of faith.

### Why Drift? Because We Love NPCs

As we stumbled upon a brilliant blog post, penned by a visionary named Lisa—a digital nomad who found Drift to be her e-commerce spirit animal—we discovered the beauty of turning static web experiences into dynamic customer conversations. Now, setting out to mimic those magical interactions she described seemed essential. Like NPCs (non-playable characters, for those who escaped the video game craze), Drift creates meaningful, real-time conversations, adding a human touch in an automated world. We wanted that—not just for our site but for our sanity.

### Step 1: Code It Like You Mean It

The first hurdle was embedding Drift’s widget. Luckily, armed with Lisa’s guide, we accessed Drift’s dashboard and located our unique "embed" code. Simple enough? Sure. We copied it, then ventured over to our e-commerce backend—imagine cramming a note into your personal library of carefully curated code. We inserted it, plain and quick, right before the closing `<body>` tag. Suddenly, our website wasn't just a collection of words and pictures but something alive. Like Frankenstein's monster, but friendlier and far less dizzying.

```html
<!-- Drift Widget Code -->
<script>
  !function() {
    // drift snippet
    var t = document.createElement("script");
    t.type = "text/javascript", t.async = !0, 
    t.src = "https://js.driftt.com/include/unique/userid.js";
    var e = document.getElementsByTagName("script")[0];
    e.parentNode.insertBefore(t, e);
  }();
</script>
```

### Step 2: Customize, Not Compromise

The fun part—or where creative madness took over—awaited us next. We navigated to our Drift dashboard like explorers checking their map. Customizing the widget was like choosing an outfit for a first date. Should it be blue or calming mint green? We debated colors as if they were life choices. We selected a catchy greeting message, something personal, like "Hey there! Need help with your adventure?" Customization: it's not just about aesthetics; it's about setting the scene for customer journeys that matter.

### Step 3: Automate Like a Pro—or Attempt To

Remember when machines were the future? Well, they’re very much the now. Drift's automation was ready for us to tackle next. Despite a few brow-raising moments of misunderstanding the flow builder, we managed to set up a playbook—aka, Drift's version of the Wizard of Oz, pulling levers behind the curtain. We arranged triggers for site visitors based on their needs. Shopping for socks? "Hey there! Check out our cozy collection!" Browsing without sales intrigue? "Guess what, your perfect match is on sale!"

### Reflecting, Laughing, Learning

With Drift in place, our website wasn't just ticking boxes for what an e-comm site should do—it was engaging, interacting, and frankly, becoming a friendlier place. Did it give us omnipotent retail powers? Not quite. But setting it up, learning from bobbles (and Lisa's fun mishaps), and plugging away with more confidence than before—these were the invaluable rewards. In the end, around our digital campfire, we laughed, we learned, we connected—and that was Drift’s greatest gift.

