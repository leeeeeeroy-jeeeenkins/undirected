---
slug: how-to-use-drupal-as-a-headless-cms
title: How to Use Drupal as a Headless CMS
authors: [undirected]
---


# How to Use Drupal as a Headless CMS

Ah, Drupal. Before diving into the ins-and-outs of Drupal as a headless CMS, let me share this quirky tale. Picture a small, well-lit room, back in 2016 at a cozy tech meetup. There was Alex, an enthusiastic Drupal developer with glasses perpetually perched on his head rather than his nose. He had a knack for turning the mundane into magic. One day, as we gathered around a messy whiteboard scrawled with indecipherable notes, Alex looked up, eyes twinkling, and said, "Let's unleash Drupal. Let's make it sing!" That, dear friends, was the spark—the moment we decided to explore the wacky but wonderful world of headless Drupal, like rebellious developers in an open-source rock band.

Now, let's embark on this journey together and channel our inner Alex. Grab yourself a warm cup of tea, or coffee if that's more your thing, and let’s dive into the realm of Drupal as a headless CMS.

## Setting the Stage: Understanding Headless CMS

Before we start deconstructing the head of our beloved Drupal, let's reminisce back to that meetup. There was this fellow, Natalie, who boldly questioned, "But why go headless?" A murmur spread across the room like wildfire. You see, a headless CMS is both an irresistible mystery and a practical solution. Imagine your CMS as a content chef, lovingly crafting your digital recipes—which it then passes to another to plate. It's still Drupal, just with a snazzier haircut.

### Why Go Headless?

Remember when Natalie asked why? Alex’s response was simple but thought-provoking: "Flexibility, Natalie. Freedom." With a headless CMS, content is liberated from presentation. It whispers sweet promises to front-end technologies, like React or VueJS, allowing them to do their thing without shackles. It means faster development cycles, more dynamic user experiences, and a kind of digital harmony that typically results in developers doing an unplanned celebratory jig.

## Setting Up Drupal as a Headless CMS

And now, onto the remedy itself. How do we trim this Drupal dragon into a sleek, headless form? The process, much like baking a perfect soufflé, involves a series of precise steps. No rushing.

### Step 1: Installing Drupal

First, install Drupal. It’s foundational, like the flour in our predictive soufflé analogy. We all gathered with bated breath as Alex adeptly spun up a new installation. If you're new to this, worry not, we have your back.

```bash
composer create-project drupal/recommended-project my_headless_drupal
cd my_headless_drupal
```

Look at us, all composer-savvy! Next, set up your database. Remember to breathe; let’s not get that heart rate too high.

### Step 2: Launch Your Drupal Site

With the curry – ahem, Drupal – base in place, go ahead and launch the setup wizard. It feels like a gentle stroll compared to the feats we’ll accomplish soon.

```shell
php -S localhost:8888 -t web
```

You’ll find your localhost dancing at port 8888. Set the database credentials, wizard through the prompts, and voilà!

### Step 3: Enable RESTful Web Services

Oh, REST services, the strings that will allow you to puppeteer Drupal’s content like the master developer you are. Navigate to “Extend” in the admin menu and flutter over these modules: RESTful Web Services, JSON:API, and Serialization.

Once activated, your Drupal instance will be set up to serve as a delicious content buffet, accessible to whichever front-end revelers you invite.

## Building the Bridge: Connecting Front End

So, here we were once more—a huddle of developers with caffeine coursing through our veins. Our goal: to connect our freshly headless CMS with a dazzling front-end application.

### Step 4: Fetch Content via API

We need to verify the dance between Drupal and its admirer—our chosen front end. For this, the magic wand is cURL or Postman; a touch quaint, but reliable.

```bash
curl http://localhost:8888/jsonapi/node/article 
```

Let yourself be serenaded by a JSON response; it’s the sweet, syrupy success of connectivity.

### Step 5: Integrate with a Front-End Framework

Alex had chosen React for this personal Sonata. There was something about its component-based harmony. But could be anything: Angular, Vue, Svelte, or even vanilla JS if you’re into retro.

In React, perhaps you'd do something like this—brace yourself, code ahead:

```javascript
import React, { useEffect, useState } from 'react';

function App() {
  const [articles, setArticles] = useState([]);

  useEffect(() => {
    fetch('http://localhost:8888/jsonapi/node/article')
      .then(response => response.json())
      .then(data => setArticles(data.data));
  }, []);

  return (
    <div>
      <h1>Articles</h1>
      <ul>
        {articles.map(article => (
          <li key={article.id}>{article.attributes.title}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

The bridge is built. Now, sit back for a moment and observe. Revel in the symphony of your creation, one that Alex—with his endearing passion—knew was possible.

## Challenges Along the Way

Our tech story wouldn’t be complete without the little gremlins trying to disrupt it. One day, Sarah, a fellow enthusiast, exclaimed over her laptop’s glowing screen, “The JSON isn’t loading!” That was a sharp learning moment: we learned about the quirkiness of CORS settings and how they craved proper configuration.

### Step 6: Configure CORS in Drupal

Scroll, click, and breathe. Declutter the path for your endpoints by editing the `services.yml` file. It may seem like a cryptic tome, but hold our hand—metaphorically.

```yaml
cors.config:
  enabled: true
  allowedOrigins: ['*']
  allowedHeaders: ['Accept', 'Content-Type', 'Authorization']
  exposedHeaders: true
  allowedMethods: ['GET', 'POST', 'PATCH', 'DELETE', 'OPTIONS']
  maxAge: 1000
```

Revel in the thrill of settings-turned-right. 

## Bringing It All Together

Let's take a step back and bask in what we’ve constructed—to breathe the fragrance of our dish, the delicate soufflé that is headless Drupal. We’ve spun it up, REST-ified it, and affiliated it with a buzzing front end. As with all tech adventures, we bonded over challenges, learned from them, and shared giggles over those unavoidable errors.

To conclude, remember our yarns woven through this narrative, the laughter, Alex’s love for digital symphony, and the camaraderie of a team making Drupal dance to this different tune.

Someday, when you're enjoying a moment of victory, think back to our journey and, perhaps, raise a glass of your favored brew in honor of the wonderful world of headless Drupal—and to Alex, the original dreamer, who set us on this delightful path.

Cheers to shared stories and more headless adventures! 