---
slug: optimizing-brightcove-player-for-mobile-devices
title: Optimizing Brightcove Player for Mobile Devices
authors: [undirected]
---


# Optimizing Brightcove Player for Mobile Devices

Once upon a time—or to be precise, one sweltering summer afternoon—I found myself huddled in a nondescript café, the kind with overpriced espresso and Wi-Fi that only worked if you sat next to the kitchen. Hidden beneath a mosaic of unpaid bills and scribbled notes, my laptop stood valiantly, trying to live up to the impossible promise of seamless video streaming. There I was, alongside my seasoned tech-enthusiast friend Cameron, tangled in the noble pursuit of optimizing the Brightcove Player for mobile devices. Cameron had the usual gleam in his eye, the one reserved for the passionate discourse on pixel density and data buffering. It made our quest feel more like an epic tale than a struggle against lag and buffering wheels.

Fast forward ten cups of coffee and a multitude of Ctrl-Zs later, emerged the first glimmer of victory—snappier videos on mobile screens. The magic wasn’t in massive overhauls but rather in the gentle chiseling of the player’s settings; each tweak revealed a more fluid, vibrant viewing experience. So, as we embark on this adventure together, let’s explore the artistry of optimizing Brightcove Player for the small screen.

## The Initial Foray into Settings Rendering

It was Cameron who suggested, over a croissant that threatened to crumble into oblivion, that we should first delve into the player’s rendering settings. "It’s like giving your player the right shoes," Cameron said. He wasn’t wrong. Ensuring the player starts on the right foot—think responsive design—is clutch. We danced through the code, altering configurations as if weaving an intricate tapestry.

### Step 1: Embrace the Responsive Design

Responsive design isn’t just a buzzword; it's akin to a universal translator for media files. Ensuring our Brightcove Player could adapt to any screen, we initiated the key settings:

```javascript
videojs('example_video').ready(function() {
  var myPlayer = this;
  myPlayer.width(window.innerWidth);
  myPlayer.height(window.innerHeight);
});
```

This script allows the player to adapt dynamically to screen size, thus honoring the device's dimensions with grace.

### Step 2: Fluid & Flexible Skin

It turns out that players, much like turtles, appreciate a nice shell. We adjusted the player skin to breathe with flexibility, helping videos glide with elegance.

```css
.video-js .vjs-control-bar {
  display: flex;
  flex-wrap: wrap;
}
```

The blend of functionality and simplicity had, surprisingly, calming results on both the player and my own caffeine-fueled nerves.

## Touch Sensitivity: The Unsung Hero

Cameron, balancing his phone on a precarious stack of napkins, demonstrated—through a fervor only matched by late-night infomercials—the importance of touch sensitivity. On mobile screens, touch is the language the player must speak fluently.

### Step 1: Enhance the Interaction

We dove into touch interaction adjustments. This is where our library of gestures came alive:

```javascript
myPlayer.on('tap', function() {
  if (myPlayer.paused()) {
    myPlayer.play();
  } else {
    myPlayer.pause();
  }
});
```

After some adjustments, taps became more effective than a morning double espresso.

### Step 2: The Swipe Revelation

Swiping wasn’t just for dating apps. Oh no, in our realm, it became a key player interaction:

```javascript
myPlayer.on('swipeleft swiperight', function() {
  myPlayer.currentTime(myPlayer.currentTime() + (event.direction === 'left' ? -10 : 10));
});
```

We chuckled—perhaps more out of relief than anything else—as we realized that touch navigation was less labyrinth and more walk in the park now.

## The Art of Compression and Bitrate Roulette

There was a moment, a quiet pause in our relentless tinkering, when the importance of compression dawned like a revelation across the remnants of our café table. Compression, when crafted with discernment, could spell the difference between a smooth stream and a slideshow.

### Step 1: The Compression Dance

“Less is more,” Cameron chimed, surrounded by an assembly of video files waiting for their weight-loss transformation. We infused our process with transcoding wisdom:

```bash
ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4
```

The leaner files danced through networks with the grace of a prima ballerina.

### Step 2: Bitrates – The Great Balancing Act

This was Jenga at its finest. We adjusted bitrate settings, seeking that sweet spot between quality and bandwidth.

```javascript
{
  "playlist": [
    {
      "sources": [
        {
          "src": "video_720p.mp4",
          "type": "video/mp4",
          "bitrate": 2000
        },
        {
          "src": "video_480p.mp4",
          "type": "video/mp4",
          "bitrate": 1000
        }
      ]
    }
  ]
}
```

The harmony between sharp visuals and streaming continuity left us cheering into the encroaching dusk.

## Cache Magic & The Road Less Buffered

The epitome of our saga came when Cameron, almost nonchalantly, began speaking of cache. Cache, so to speak, doesn’t have the allure of immediate gratification but instead offers the tranquility of consistent performance over time.

### The Caching Lullaby

It was like leaving cookies for the browser, a gift we hoped would return in kind. With a little configuration, our cache strategy emerged:

```javascript
{
  "cache": {
    "expiration": 3600
  }
}
```

Videos would sidestep buffering pitfalls, navigating elegantly through the internet murk. Our player had found its groove.

## Triumph in a Café Corner

As our adventure wound down, the café morphed into more than a mere backdrop. It harbored our triumphs, witnessed the fumbling slew of errors turned solutions, and in its camaraderie, helped tweak our journey. Our Brightcove Player had not only survived but thrived on mobile devices.

So, here we part, dear compatriots. May our shared tale inspire a dance with your own code and digital avatars. Remember, optimization isn't just a task—it's a celebration. As Cameron would say with a mischievous wink, "May your videos never buffer, and may your scripts always compile. Cheers!"