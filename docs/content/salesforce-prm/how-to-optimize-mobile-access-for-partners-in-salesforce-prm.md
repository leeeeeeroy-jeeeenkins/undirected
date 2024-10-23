---
slug: how-to-optimize-mobile-access-for-partners-in-salesforce-prm
title: How to Optimize Mobile Access for Partners in Salesforce PRM
authors: [undirected]
---


# How to Optimize Mobile Access for Partners in Salesforce PRM

I remember the moment like it was yesterday. It was a Tuesday afternoon in early spring. You know, the kind of day where the breeze feels like it's whispering secrets as it passes by. I sat with my coffee cup warming my hands. That’s when I got the call. Sarika from our marketing team—always energetic, always a little flustered—wondered aloud why our partners couldn’t easily access Salesforce PRM on their mobile devices. In an instant, the tranquility of the afternoon was replaced with the hum of urgency. And just like that, our journey to optimize mobile access for our partners had begun.

## Reflecting on Our First Steps

The initial steps were disjointed, clumsy even—think of trying to solve a puzzle in the dark, with mittens on. But progress is progress, no matter how inelegantly achieved. We realized quickly that we needed to engage ourselves fully with the tools Salesforce offers, and that's exactly where things got interesting—or depending on my mood, slightly maddening.

### Step 1: Recognize the Gravity of Mobile Access

If you've ever caught yourself scrolling through your phone instead of working (we've all been there), you’ll realize the significant impact mobile accessibility has in our lives. Salesforce PRM, built on the robust Salesforce Platform, can be a clunky beast if not properly optimized for mobile. Here we were, failing to leverage this amazing tool because our partners couldn’t access it conveniently. This realization was both a relief and a spark—a reminder that modern business must meet people where they are: on their phones.

**Plan of Action:**
- Grasp the urgency. Partners need information at their fingertips.
- Know that frustration will lead to expediency. It’s like suddenly remembering that cookies are in the oven.

### Step 2: Review and Customize Mobile Navigation

For pure transparency, there was a time when mobile navigation was, shall we say, the wild west. But customizing it in Salesforce PRM? That's where our sense of exploration really gained momentum.

We began by nibbling away at the edges—exploring the Salesforce App Builder. It was here, amidst the click and drag, that I had an epiphany: customization was our golden ticket. Imagine being an artist with an infinite palette. Critically, we examined the tabs and components to ensure they were truly indispensable for our partners’ experiences.

**How We Did It:**
1. **Open Salesforce App Builder**: We navigated to Setup, found the App Manager, and selected the PRM app.
2. **Click on Mobile Navigation**: Modify and drag the essential items over to the Mobile Navigation pane, ditching the non-essentials—because minimalism is key.
3. **Test, Tweak, Treasure**: We published changes, tested on different devices, and repeated till it felt as natural as a stroll in the park.

Oh, and don’t forget to communicate changes to the partners, unless you relish puzzled phone calls.

### Step 3: Utilize Mobile Lightning Components

Once, as we delved deeper into optimizing experience, a thought struck me: aren’t Lightning Components just like LEGO blocks? Well, that analogy holds—at least it guided us. Because our goal was to provide flexibility and ease akin to building with those classic, childhood bricks.

Our journey to understanding involved leveraging out-of-the-box components only at first—to learn the ropes—before attempting to develop custom components that would perfectly suit partner requirements.

**The Nuts and Bolts:**
- **Identify Essential Components**: Begin with standard offerings like tabs, dashboards, etc.
- **Experiment with Custom Ones**: Use code to craft unique experiences. This demands a fair bit of technical knowledge which was, in our case, acquired through trial, error, and a few cups of strong tea.

Example code might look like this:

```javascript
import { LightningElement, track } from 'lwc';

export default class CustomComponentExample extends LightningElement {
  @track message = 'Hello, partners!';

  handleChangeMessage(event) {
    this.message = event.target.value;
  }
}
```

### Step 4: Prioritize Speed and Performance

Recall those snail-paced internet days? It was somewhat like that with slower mobile access. But calling it merely frustrating would be generous. It was wake-up-three-hours-early stressful. So, a snappy performance became predominant on our priority list.

Now, I’ll be honest: monitoring performance metrics and optimizing load times came across as tedious, but by golly, it’s like polishing a diamond—necessary and extremely satisfying—even if we were pushing our technical chops to the limit.

**Tools & Techniques:**
- **Salesforce Performance Test**: Regularly run tests to analyze and learn where bottlenecks occur.
- **Effective Caching**: With proper caching strategies—if you have solid access to the labs—we ensured swift repeat visits.
  
### Step 5: Training and Support

Here's a little secret—partners are like the directors of their own stories. They deserve both roles in the explanation and engagement departments. We found that partner feedback, always rich in insight, is the secret ingredient of any harmonious relationship. And training is not to be undervalued—it's like baking a cake with love as the main ingredient.

Yet remember: patience is a virtue when dealing with the inevitable “how does this work again?” questions. Reiterate walkthroughs, provide guides, possibly even video tutorials—anything that will make them pros and embolden us as savvy navigators.

## Epilogue: A Little Wiser and Lighthearted

At the end of our odyssey, our partners were engaged, efficient, and happier than a dog off its leash. Alas, it wasn't a miracle. We dared to face the reality of digital transformation—it’s ongoing and ever-evolving.

With every new Salesforce update, there’s a bit of a dance—a tango with transformations, shifts, and sudden realizations. Yet what could be more thrilling than being at the threshold of innovation, mobile phones in hand, ready to shape new experiences and cultivate stronger relationships?

Optimizing mobile access for our partners didn't just improve user experiences; it strengthened our community. You see, this journey made us discern that the essence of partnership is like the sun—underrated when good, indispensable when great.

In the end, we're left with the shared wisdom of improvement and an invitation to continuous exploration. So, shall we? Grab your toolkit; let's lead this adventurous dance anew.