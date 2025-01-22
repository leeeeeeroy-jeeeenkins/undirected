---
slug: how-to-integrate-brightcove-with-adobe-experience-manager
title: How to Integrate Brightcove with Adobe Experience Manager
authors: [undirected]
---


# How to Integrate Brightcove with Adobe Experience Manager

Gather 'round, dear reader, for a spirited tale of integration, imagination, and innovation. This story—our story—begins not in the sterile confines of a corporate conference call, but amidst the aromatic swirls of freshly brewed coffee in a cozy café, where caffeine and creativity often dance hand in hand. On a sun-dappled afternoon, my friend Alex—a seasoned developer and espresso enthusiast—approached with a conundrum that might sound familiar to anyone caught in the chimeric crossroads of content management and video strategy.

"We've got this wild idea," Alex enthused, eyes twinkling with possibility. "What if we could take our video library from Brightcove and weave it seamlessly into Adobe Experience Manager?" A lofty ambition, akin to merging two musical virtuosos into a harmonized duet. Little did we know, this endeavor would evolve into a journey full of digital serendipity. So let’s embark on this adventure together, armed with curiosity and a sense of humor, all the while keeping jargon at bay.

## The Prelude: Understanding Our Tools

Before we dive into code and configurations, dear comrades, let’s pause to appreciate the beauty of our tools. Brightcove, our illustrious video platform, like the grand old cinematics of yore—captures, hosts, and delivers video content with aplomb. Imagine a sprawling library of films, at your fingertips, whispering endless possibilities.

In tandem, Adobe Experience Manager (AEM) stands resilient—like a cathedral of content—an amazing solution for managing and delivering digital experiences. Architecturally formidable, yet welcoming to those who dare to build functional aesthetics.

**The Key Players:** Like meeting the protagonists in an epic saga, understanding what we're working with helps light our path. Our task—no mere trifle—is to coax these titans into a synchronized ballet.

## Act I: Setting the Stage

We began our venture one bright morning—armed with a laptop, a vivid imagination, and a generous dollop of optimism. Preparation, as they say, is the key to successful integration, and we were on it like a bee on a blooming flower.

### Step 1: Access Credentials

First order of business: letting Brightcove know we mean business (and have legitimate access). We started by rolling up our sleeves and grabbing our API credentials from Brightcove’s studio. This data dance starts with a login—name, password, secret handshake—simple, yet sacred deeds. Go to your Brightcove account, find API Authentication. There they are: Client ID and Client Secret—your dynamic duo.

```plaintext
Client ID: xxxxx
Client Secret: xxxxxxxx
```

Safeguard them like precious heirlooms, for these will open the vaults of your video content unto AEM.

### Step 2: Preparing Adobe Experience Manager

We switch our focus—as swiftly as a magician shuffles cards—to AEM's side of the equation. Our main objective? Ensure AEM is primed, prepped, and patiently waiting for an influx of video content.

- **Setting Permissions:**
  Everyone needs permissions in this world—even systems. Inside AEM, we ensure our user has the right permissions to interact with external services. A stroll through the Access Control list is all it takes.

- **Creating a Service User:**
  A special kind of user that deals with integrations like a suave hotel concierge handling requests with poise. Go to `Tools > Security > Users`, create a new Service User named ‘brightcove-service-user’. Now, AEM is ready to boogie with Brightcove.

## Intermission: A Humorous Twist

As we tinkered with settings and checked configurations, a humorous realization struck us—like a cat startled by its own reflection. The act of integration, in its essence, mirrors a blind date. Two unknowns meet, hoping to find compatibility and a spark—sometimes dazzling, sometimes disastrous. 

A stuttering script or a misplaced semicolon could thwart our well-laid plans, leaving us to laugh (occasionally cry) at the idiosyncrasies of code.

## Act II: Building the Bridge

With our players prepared and permissions in place, it was time to fashion bridges between lands—connecting Brightcove to AEM.

### Step 3: API Connection

Our mission: convince AEM to converse with Brightcove over cyberspace. This requires a connector, like translating between tongues—English and binary—so both parties understand each other.

- **Creating the Connector:**
  We head into AEM and create a custom workflow using the Workflow Models tool. Add a process step, name it majestically, and set its process to "Inject Brightcove Videos". This process will later become the foundation of our video liberation.

- **Configuring HTTP Client:**
  In the same breath, we tend to the HTTP Client, configuring it mindfully to talk with Brightcove via a secure HTTPS handshake. It's HTTPS or bust around here—cybersecurity demands nothing less.

```xml
<Configuration>
  <user>brightcove-service-user</user>
  <password>verysecurepassword</password>
  <timeout>60000</timeout>
</Configuration>
```

### Step 4: Testing Connections

Before trundling onward, we take a moment—a peace pipe interlude—to test our connections. There’s nothing more deflating than discovering a dysfunctional script post-launch. A simple, yet honest test with a Brightcove video API call from AEM ensures our bridge holds strong.

- **Troubleshooting:**
  Errors, here they come! Logs are our guide in this dark debugging labyrinth. We decipher the cryptic messages AEM provides when connections falter—often a misplaced character or forgotten configuration. Patience, grasshopper, patience.

## Act III: The Grand Integration

We’ve come a long way, shared laughter over inconvenient bugs, and now stand on the brink of true integration—a breath away from realization.

### Step 5: Importing Videos

The time had come. Brightcove videos needed ushering into AEM.

- **Custom Integration:**
  We dive headfirst into AEM’s Digital Asset Manager (DAM), where our workflow wizardry from earlier clicks into action. Our custom workflow probes Brightcove’s media repository, fetching videos with grace and depositing them into AEM like gifts from the technological gods.

```java
// Java snippet to execute the video import
public void importBrightcoveVideo(String videoUrl) {
    // Perform API calls and asset management tasks
}
```

### Step 6: Seamless Display in AEM

Now that those delightful videos nestle comfortably within AEM, it's about making them shine.

- **Component Creation:**
  We embark on crafting a custom AEM component—a digital artisan’s touch. This component allows AEM pages to display Brightcove videos beautifully, using templates and styling that complement the surrounding content.

```html
<div class="brightcove-video">
  <video src="(video-source-url)"></video>
</div>
```

### Step 7: The Final Flourish

Just like the ending of a cinematic masterpiece, we conduct a final review—like film critics assessing an Oscar contender.

- **Testing Display:**
  It's crucial to rigorously test the video display across different devices, browsers, and internet conditions. We load pages like excited toddlers unwrapping gifts—ensuring videos play smoothly, without a hitch or stumble.

## Epilogue: The Joy of Integration

The coffee-stained table at our café served as a witness—a silent chronicler of our mighty endeavor. As we witnessed Brightcove’s videos playing seamlessly within AEM, a sense of accomplishment—like completing a complex jigsaw—embraced us.

Our integration tale, though whimsical and wrought with trials, taught us the invaluable lesson of persistence, creativity, and teamwork. And perhaps next time, let’s tackle it over cappuccinos with extra froth.

In the exaggerated words of our mentor, Kevin, "When code aligns, it’s akin to watching a sunset—beautiful, inevitable, and slightly surreal." Here’s to the wild digital adventures that await us, dear friends. May we always find delight in blending the unblendable.