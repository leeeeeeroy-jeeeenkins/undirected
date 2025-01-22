---
slug: how-to-set-up-multi-device-streaming-with-brightcove
title: How to Set Up Multi Device Streaming with Brightcove
authors: [undirected]
---


# How to Set Up Multi-Device Streaming with Brightcove

There we were, Steve and I, on a chilly autumn afternoon, huddled around a warm mug of cocoa trying to wrap our heads around the digital beast that is multi-device streaming. Our challenge was simple yet daunting: to breathe life into a seamless streaming experience using Brightcove that would work on everything from phones to smart fridges — if that’s even a thing. Our goal: to help our little town theater make its indie films accessible to the world — or at least to anyone with an Internet connection. As we unraveled the mysteries of the Brightcove platform, it felt like embarking on a digital odyssey. With each hurdle, we learned not just the mechanics, but the art of streaming. So, buckle up as we share our tale. 

## Begin the Journey: Unearthing Brightcove

It all started with a simple login. Steve, ever the tech whisperer, cracked his knuckles and logged into Brightcove Studio, our new command center. It's like peering into a cockpit with digital dials and switches at your fingertips — a digital haven. We were greeted by a dashboard that reminded us of the control panel of the Starship Enterprise, sans the warp drive buttons. With a shared glance, we knew it was time to take off, navigating through tabs with the grace of a gazelle on an ice rink.

### Step 1: Crafting a New Player

Our first mission: creating a player. Imagine it as the shiny box where your videos will dance. The Brightcove Studio welcomed us in with open arms. To start, we clicked on the "Players" section. It was like being at a video arcade, with rows of options beckoning. We hit "Add New Player," kissed those default settings goodbye, and decided to customize. Naming our player "IndieFlicks" felt right, as if we were giving it a soul. 

```json
{
  "name": "IndieFlicks",
  "configuration": {
    "autoplay": true,
    "mute": false,
    "controls": ["play", "volume", "fullscreen"]
  }
}
```

Steve loved data, much like a squirrel loves acorns. He insisted on activating the analytics feature to track viewer engagement — we need metrics, he said, or you're flying blind. And so, with a few clicks, IndieFlicks was ready to shine like a newly minted coin.

## Uploading the Magic: Adding Video Content

At this point, I felt like an aspiring magician without a wand. The good stuff — our video content — needed to be uploaded. We ventured over to the "Media" section, brightly lit and inviting as if saying, "Bring me your films!" In that moment, the upload button was mightier than the legendary Excalibur.

### Step 2: Upload & Organize Videos

We clicked "Upload" with our heartbeats a half-second faster, selecting files with the anticipation of unwrapping a surprise gift. Brightcove offered a comforting pat on the back by supporting multiple formats. Films loaded faster than gossip at a family reunion, and once in, it was time to organize with tags and playlists — ensuring no film was left behind in the digital wilderness.

```json
{
  "title": "The Great Escape",
  "tags": ["adventure", "indie"],
  "playlist": "Featured Movies"
}
```

Tina, our fellow cinephile and playlist curator, suggested categorizing them dexterously. As an art form, each playlist was named and ordered like a lovingly crafted mixtape — “Evening Calm,” “Adrenaline Rush,” helmed the experience.

## Customizing the Experience: What’s a Player Without Personality?

I’ll admit, customizing the player was initially as baffling as choosing the right shade of white paint. Steve, the artiste, insisted on tweaking the CSS to retain our brand’s ethos — bold yet understated. We dove into the realm of customizable settings, which felt like adjusting the ingredients of a secret family recipe. 

### Step 3: Style the Player

With trembling fingers, we accessed the player settings and moved into the "Advanced" section. Here, we could alter the visual styles, akin to deciding whether your ice cream needs more sprinkles. We chose wisely, never crossing into the gaudy, but infusing a touch of personal flair. 

```css
video::-webkit-media-controls {
  background-color: #000000;
  color: #ff9900;
}
```

We added custom colors, using our brand’s vibrant palette — making it pop yet restrain itself like a well-behaved lava lamp. And thus, a simple player became our canvas, our masterpiece ready to be shared with the world.

## Connecting the Dots: Enabling Multi-Device Streaming

Our films now stood polished, ready for their audience like actors waiting in the wings. The next goal, and possibly the most crucial, was to make sure these actors could perform on any stage — phones, tablets, even your grandma's old television set.

### Step 4: Enable HLS and DASH

The magic words were HLS (HTTP Live Streaming) and DASH (Dynamic Adaptive Streaming over HTTP). These protocols vowed to ensure uninterrupted streaming across devices — much like a benevolent wizard casting the omni-device spell. Under the "Settings" tab, we enabled both as Steve quipped, “Our videos are now Dumbledore-approved.”

```json
{
  "hls": true,
  "dash": true
}
```

Steve emphasized a steady internet pipe was key — you can't just funnel Niagra through a garden hose. After some bandwidth hand-wringing, we reached content nirvana — spread across phones, tablets, and whatever other rectangles our viewers had.

## Testing the Waters: Trial by Fire

The moment of truth. Our setup was complete, but would it hold under the scrutiny of our first live test? The anticipation was electric. We scheduled a live stream, one of our proudest film releases — The Great Escape — and sat glued to our screens like kids awaiting santa.

### Step 5: Launch a Live Event

With an online calendar more colorful than a field of wildflowers, we set the date and time. Clicking “Schedule Event,” we watched the magic unfold. Brightcove eased our nerves, letting us preview the stream — as comforting as peering into a warm oven filled with baking cookies.

```json
{
  "event": {
    "title": "The Great Escape Premiere",
    "scheduledTime": "2023-05-01T19:00:00Z"
  }
}
```

Cathy, our town’s web wizard, made sure the stream link was shared widely and wildly. Friends, family, maybe a few enemies would now watch and — fingers crossed — enjoy.

## The Encore: Ensuring a Seamless Experience

But you don’t just set and forget. A wise barista once told me, “The best brew needs attention to the last drop.” Steve concurred, advocating for a final test of latency, buffering, and device compatibility with the thoroughness of a super-spy diffusing a bomb.

### Step 6: Monitor & Optimize

During our stress test, we huddled over analytics, making adjustments like crafty baristas honing their beans. We adjusted bitrates and optimized network conditions — because buffering during a climax is the worst plot twist. Our final act involved gathering feedback from viewers, refining the process until it was buttery smooth.

```json
{
  "analytics": {
    "watchTime": "95%",
    "bufferingRate": "less than 1%"
  }
}
```

With our indie theater's newfound reach, the screen was set, the stage was ours, and as we sat back in our creaky seats — steaming cocoa in hand once more — we marveled at our journey.

And so, there you have it. From figuring out the first steps, to coding players and wrestling with bitrate demons, we've hopefully shared a guiding light on your very own multi-device streaming journey with Brightcove. Now, go forth and give your videos the audience they deserve.