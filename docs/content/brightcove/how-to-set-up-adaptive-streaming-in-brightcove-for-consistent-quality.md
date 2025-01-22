---
slug: how-to-set-up-adaptive-streaming-in-brightcove-for-consistent-quality
title: How to Set Up Adaptive Streaming in Brightcove for Consistent Quality
authors: [undirected]
---


# How to Set Up Adaptive Streaming in Brightcove for Consistent Quality

Let me take you back a few years ago when we were on the cusp of an event that shaped not just my understanding of video streaming but also our shared vision of what digital content should look like. It was one of those fall evenings, pumpkin spice lattes in hand, that our small team huddled together in that cramped office with barely enough room to swing a cat. We had just launched our very first live event — a grand affair meant to reach thousands. Instead, we were welcomed with a pixelated, buffering fiasco that made watching paint dry seem thrilling by comparison.

Our viewers weren’t happy. "Where’s the consistency in this quality?" read one despairing comment, and if you could hear a collective sigh over the internet, that was it. 

That night, we vowed never to be defeated by streaming woes again. Enter Brightcove — our savior in the form of a sleek, intelligent platform promising adaptive streaming nirvana. Here I'll share how we managed to conquer adaptive streaming setup in Brightcove, creating a consistently high-quality viewing experience that would make even the most cynical viewers grin like Cheshire cats. Journey with me through this odyssey, and let's uncover how this feast of digital delights is made.

## Unpacking the Adaptive Streaming Treasure Box

As we fired up our computers the next morning, with the enthusiasm of caffeine-driven explorers, the first task was to understand what "adaptive streaming" actually meant. It was like opening a treasure box, with each element designed to ensure our video content never looked like a scene from an 8-bit game again. In simpler terms, adaptive streaming dynamically adjusts the quality of a video stream in real-time, based on a viewer’s internet connection — kind of like water flowing into various streams around rocks and pebbles, adapting to every curve and turn.

### Accessing Brightcove's Video Cloud

Before we did anything else, maybe even before taking a sip of that second latte, we needed to access Brightcove’s Video Cloud interface — our command center for this particular mission. Logging in felt strangely empowering, a portal into a universe of video possibilities. We went to `video.brightcove.com` and entered our credentials, ready to tame this beast.

Navigating to the Media Module interface, with its sleek look reminding us we were dealing with top-notch tech, we could feel the control at our fingertips. This is where we would manage our vast trove of video content, ensuring it was optimized for the masses to devour in all its glory.

### Crafting the Renditions

Steph, our go-to media expert — the Gandalf of our video adventures — pointed out that creating multiple renditions was key. “Think of it like preparing different dishes for a fancy dinner,” she mused. “You want something for everyone — the small bites, the hearty entrees, and everything in between.”

In Brightcove, these different dishes are video renditions. We clicked on the **Profiles** tab, like eager chefs ready to prepare a feast, and selected our default profile. There, we set up the multiple renditions that are vital for adaptive streaming.

```json
{
  "renditions": [
    { "height": 240, "video_bitrate": 400 },
    { "height": 480, "video_bitrate": 1000 },
    { "height": 720, "video_bitrate": 2500 },
    { "height": 1080, "video_bitrate": 4500 }
  ]
}
```

Our choices were based on the most common devices and network connections of our audience. Better yet, Brightcove’s smart encoding did most of the heavy lifting for us — no magic wands required.

### Time to Play with RTMP and HLS

Once our renditions were good to go, it was time to decide on the types of streams we’d use. Remember back in the day when options were either black and white or color? Streaming is a bit like that, only with more acronyms — let’s bring out the RTMP and HLS.

HLS (HTTP Live Streaming) is our dependable friend, especially useful for mobile and web platforms. It’s like the reliable car that never fails you, always ready to cruise smoothly no matter the terrain. We ensured that all our renditions were HLS-compatible, providing smooth transitions that left zero space for complaints.

RTMP (Real-Time Messaging Protocol) feels more like the sports car — slick, fast, and occasionally tricky. Perfect for platforms that need ultra-low latency, like live events. Setting this up in Brightcove, under the **Publish Settings**, involved checking the right boxes, quite literally.

```yaml
publish_settings:
  formats:
    - hls
    - rtmp
```

Our setups were inclusive enough to make sure every viewer — whether on a desktop treadmill or waiting for a train on mobile — had a ride as smooth as silk.

### Testing the Waters or Streams

Something Steph once told us stuck like gum on a shoe. “You can’t cook a dish and simply hope it tastes good,” she laughed, clearly thinking of that one curry fiasco. Testing became our friendly flavor check. And with Brightcove, this was made easy through the **Preview** function.

We clicked on our freshly encoded video, feeling a mix of anticipation and a hint of anxiety, watching it on different network speeds and devices. From 4G to Wi-Fi — we made sure to leave no stone unturned.

Problems? Of course, there were. Buffering issues on a slower connection often stuck out like a sore thumb, requiring us to tweak bitrates or maybe add a lower rendition. But with each correction, our stream quality molded into perfection.

## The Victory Lap

When our first successful stream went live without a hitch, cheers erupted like the first night fireworks. Remembering the buffering mess that kept us awake shamefaced and bleary-eyed? This was the sweet, sweet nectar of success. We'd climbed that mountain, and the view was phenomenal — digitally speaking, of course.

### Final Polishing and Futureproofing

Before we wrapped up our adaptive streaming quest, ensuring the sanctity of this setup was vital. This involved keeping up with Brightcove's updates and continuously revisiting our rendition profiles and streaming protocols. The digital landscape changes faster than we change our socks.

Adding new renditions or testing them — not because it's needed immediately but to anticipate changes in the digital ether — became part of our regular toolkit. Keeping future-ready wasn’t just about technology; it was the satisfaction of knowing our viewers, like us, adored this pixel-perfect journey.

## Wrapping It Up Like a Cherished Memory

Through our journey with adaptive streaming in Brightcove, we realized it was more than just a technical task. It was an art form, an evolving practice, much like a cherished recipe passed down through generations. We've grown together in this digital tapestry, weaving in consistency, quality, and a promise to keep delivering the best, whatever and however the future unfurls. With Brightcove by our side, we knew we were destined only for greater digital horizons. 

As we sit here, pondering over reflections and plans past and future, let’s raise a virtual toast to smooth streams ahead! Cheers to us, and to every new adventure we’ll conquer together.