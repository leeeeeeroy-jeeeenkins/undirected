---
slug: how-to-improve-load-times-of-wistia-videos-on-your-site
title: How To Improve Load Times Of Wistia Videos On Your Site
authors: [undirected]
---


# How To Improve Load Times Of Wistia Videos On Your Site

Imagine this: we're sitting in a cozy café, the aroma of coffee mingling with the warm chatter of afternoon conversations. It’s one of those days where ideas flow faster than the caffeine. We're trading stories about the curious, sometimes frustrating dance of technology. I find myself reminiscing about when I first encountered the sluggish sluggishness of Wistia videos on our site. It was exasperating. Picture this—clients tapping their fingers on the desk as the loading circle visibly mocked us on the screen.

The way that slow load time stuck in our memories—like a song we desperately wanted to forget—impacted everything from user satisfaction to our sanity. We knew we had to get to the bottom of it, and fast. With a bit of curiosity and some trial and error (cue the vision of me frantically scribbling notes while our trusted video guru, Jenny, watched on with amusement), we untangled some secrets. So, cozy up and let's dive into this together.

### The Long Wait: Discovering the Root of the Problem

Have you ever watched paint dry? Me neither, but I bet it felt a lot like waiting for those videos to buffer. One wintry afternoon, I remembered how this all started—a frantic email from a client whose patience, like the broadband signal, was thinning. We gathered 'round a laptop with steaming mugs of sanity (read: coffee), determined to unravel the mysterious sorcery behind our Wistia videos loading slower than a sloth on sedatives.

Our nemesis was revealed: poorly optimized videos. It was like trying to swim in your favorite jeans—possible, but why would you torture yourself? So, let's step bravely into the world of optimization!

### Step 1: Crack the Code of Video Compression

Video quality is a hot topic, much like debating the perfect amount of milk in your tea. Too much compression, and everything gets blurry like a Monet painting—too little, and you’re back where you started. Jenny suggested we try out the Handbrake tool. “It’s like a Swiss army knife for video compression,” she beamed.

Using Handbrake, we converted our videos into MP4 format, adjusting the resolution to an optimal size. Aim for 1080p unless your audience is watching on ancient devices or you’re channeling a retro vibe. We balanced between file size and quality like tightrope walkers, our goal in sight: faster load times without the fuzziness of a bygone VHS era.

```bash
handbrake -i input_video.mov -o output_video.mp4 --preset="Fast 1080p30"
```

### Step 2: Lazy Loading – It’s Smarter, Not Lazier

Remember that time Mark suggested we join an 'Introverts Unite' club? We laughed, realizing some pages were loading all videos at once, like extroverts at a party. This overload caused the stagnation we dreaded. Enter Lazy Loading, our new introverted hero.

By lazy loading thumbnails using a jQuery plugin or native JavaScript, we only loaded videos when they came into view. I distinctly remember the relief (and subtle high-five) as video after video loaded effortlessly, waiting in line like polite guests.

```html
<video data-src="video.mp4" controls class="lazy">
  <source data-src="video.mp4" type="video/mp4">
</video>
<script>
  document.addEventListener('DOMContentLoaded', function() {
    var lazyVideos = [].slice.call(document.querySelectorAll('video.lazy'));    
    if ('IntersectionObserver' in window) {
      let lazyVideoObserver = new IntersectionObserver(function(entries, observer) {
        entries.forEach(function(video) {
          if (video.isIntersecting) {
            for (let source in video.target.children) {
              let videoSource = video.target.children[source];
              if (typeof videoSource.tagName === 'string' && videoSource.tagName === 'SOURCE') {
                videoSource.src = videoSource.dataset.src;
              }
            }
            video.target.load();
            video.target.classList.remove('lazy');
            lazyVideoObserver.unobserve(video.target);
          }
        });
      });
      lazyVideos.forEach(function(lazyVideo) {
        lazyVideoObserver.observe(lazyVideo);
      });
    }
  });
</script>
```

### Step 3: CDNs – Our Trusty Sidekicks

Another tale from our battlefront—a day spent trekking the labyrinthine mazes of server response times. Wistia, like any video platform, benefits from Content Delivery Networks (CDNs). Imagine it as teleportation for your video data, zipping from server to user’s screen at lightning speed.

When we employed Wistia’s global CDN, it was as if weights were lifted off our shoulders (and the server’s). The load times dropped so dramatically that we wondered if the videos had developed an advanced AI consciousness and learned to run.

### Step 4: Custom Thumbnails – The Invitation Card Approach

Think of video thumbnails as inviting pictures on a dinner party invite. Wistia lets you customize these, and instead of relying on auto-generated ones like uncooked spaghetti (uninteresting and barely functional), we used sharp, enticing images that conveyed the essence of each video. Users clicked, watched, lathered, rinsed, repeated.

Customizing thumbnails was not just about engagement, it made sure our video started off on the right foot, loading properly optimized and not stuck in a processing vortex.

### Step 5: Efficient Embedding Practices

Remember our story’s beginning with those infuriating load times? Part of the magic wand we wielded lay in optimizing how we embedded Wistia videos. Instead of using plain old `iframe` tags, we explored Wistia’s asynchronously loading script embed, a perfect choice for embedding videos without delaying the rest of the page _just because videos were feeling leisurely_.

```html
<script src="https://fast.wistia.com/embed/medias/abcdef1234.jsonp" async></script>
<script src="https://fast.wistia.com/assets/external/E-v1.js" async></script>
<div class="wistia_embed wistia_async_abcdef1234" style="width:640px;height:360px;"></div>
```

### Conclusion: The Journey Back to Sanity

As the evening settled around our cozy café conversation, we basked in the warm glow of having mastered yet another technical tidbit in our internet odyssey. We knew that the road to seamless Wistia video performance was not a single path but a scenic route where each experiment and every tweak got us closer to faster load times and better user experience. Ultimately, it was about creating smoother, efficient engagement for visitors who could now enjoy content without the dreaded buffering pause.

Let’s toast to shared discoveries—those little triumphs where technology surrenders to our persistence. The journey, as often happens with our digital quests, had educated us as much as the destination itself. We closed our laptops, leaving the café with a relieved smile, savoring not just the coffee, but the satisfying sweetness of a job well done.