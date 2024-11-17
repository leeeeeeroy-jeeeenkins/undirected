---
slug: developing-applications-with-ibm-watson-and-node-js
title: Developing Applications with IBM Watson and Node JS
authors: [undirected]
---


# Developing Applications with IBM Watson and Node JS

There was this day—brighter than most—when I found myself staring into the sordid chaos of my cluttered desk, pizza crusts as ancient as my forgotten New Year’s resolutions, and a million tabs open on my browser that screamed for attention like chirpy lot of hyperactive toddlers. My mission, if I dared to accept it, was to build an application using IBM Watson with a Node.js backbone. Now, some of you might know how dragons are born out of such asinine tasks while you're courageously trying not to fall into an abyss of frustration.

This challenge arrived with my pal, Sam, who took a sip from his bottomless coffee mug and said, “Why not create an app that talks to people using AI? It’ll be like teaching a rock to sing opera.” And thus, our reckless adventure began.

## Enter the Gateway: Setting Up IBM Watson

Stepping into the world of IBM Watson is like walking into Willy Wonka's factory—minus the Oompa Loompas but with twice the cognitive crunch. Words like 'cognitive computing' can make folks run faster than spilling hot tea on themselves, but fear not! Follow this breadcrumb trail:

1. **IBM Cloud Beginnings**: Start by creating an account on the IBM Cloud. It’s free for lite versions, which is just what we need to get our feet wet. Sam always told me that free things are the universe’s way of saying "have at it."

2. **Service Creation**: Once signed in, head over to the Watson services section. Select your desired service—let's say Watson Assistant for a chatbot experience. Hit that tantalizing 'Create' button as if it were an arcade high score.

3. **Crack the Keys**: Post-creation, retrieve your API keys from the service credentials. These keys are like secret handshakes into a cool party where ideas dance and technology takes the lead.

4. **Fold the App**: Dive into the Watson Assistant and start crafting your first assistant. Think of it as nurturing a bonsai tree; precise yet forgiving. Define intents, entities, and dialogue nodes. Our assistant, whom we affectionately dubbed "ChatterSam," promptly decided to act both wise and witty, a reflection of its creators.

## Node JS: Our Trusty Engine

Node.js gleams like a shiny, ubiquitous tool capable of making miracles happen on the dullest of days. Sam once joked that Node.js could turn his grandma’s recipe box into a moon rover. So, how do we entangle Node.js with Watson for that enchanted application? Let's hit rewind a little.

1. **Node.js Bent Over Backward**: If you haven't already danced with Node.js, it starts with its installation from [Node.js](https://nodejs.org/). Dive into your terminal—resist the urge to teeter into the meme rabbit hole—and type out those commands of destiny: 

    ```
    npm install express
    npm install dotenv
    npm install ibm-watson
    ```

2. **Project Foundation**: Create a new directory for your project. Tradition has us naming it 'wonderland,' but anything cheeky could do. In your new home, initialize it with:

    ```
    npm init -y
    ```

   This command seeds your project with a package.json, akin to giving your ship a sail for open waters.

3. **Dot the Environment**: In the realm of .env files, secrets harbor—store your IBM Watson API credentials here. Your file may look like this:

    ```
    API_KEY=my_super_secret_k3y
    URL=https://api.us-south.assistant.watson.cloud.ibm.com
    ```

   Guard it like your last teaspoon of Nutella.

4. **Coding Samba**: It’s time to tango with the code. Create a server file, say `app.js`, and pen your first lines of JavaScript magic:

    ```javascript
    require('dotenv').config();
    const express = require('express');
    const AssistantV2 = require('ibm-watson/assistant/v2');
    const { IamAuthenticator } = require('ibm-watson/auth');

    const app = express();
    
    const assistant = new AssistantV2({
      version: '2021-06-14',
      authenticator: new IamAuthenticator({
        apikey: process.env.API_KEY,
      }),
      serviceUrl: process.env.URL,
    });

    app.use(express.json());

    app.post('/message', (req, res) => {
      assistant.message({
        assistantId: '<YOUR_ASSISTANT_ID>',
        sessionId: '<YOUR_SESSION_ID>',
        input: {
          'message_type': 'text',
          'text': req.body.input,
        },
      })
      .then(response => {
        res.json(response.result);
      })
      .catch(err => {
        console.error(err);
        res.status(500).send('Something went pop!');
      });
    });

    const PORT = 3000;
    app.listen(PORT, () => console.log(`Magic happens on port ${PORT}`));
    ```

   It does feel like we’re stitching a tapestry under a waxing moon.

## Conjuring Otherworldly Conversations

With our skeletal structure underway, let's find the pulse that lets chatter flow between us mortals and our virtual sage, ChatterSam. Connecting all parts is akin to building a bridge from thought to interaction with pixels and nodes.

1. **Immortal Sessions**: First, let's initialize a session with Watson. Pop this into your `app.js` to breathe life into conversations:

    ```javascript
    app.post('/session', (req, res) => {
      assistant.createSession({
        assistantId: '<YOUR_ASSISTANT_ID>'
      })
      .then(response => {
        res.json(response.result);
      })
      .catch(err => {
        console.error(err);
        res.status(500).send('Session trouble in paradise');
      });
    });
    ```

2. **Testing Waters**: Run your Node.js app, and in another terminal tab, test your API with a tool like Postman. Feel that thrill as messages go from curious fingers to Watson's digital ears. While Sam adeptly doodled its function on a napkin, it helped us understand better than any technical drawing.

3. **Juggling Front and Back**: Pair this back-end grit with a simple front-end that sends requests to your Node server. HTML and JavaScript will suffice—clarity over flamboyancy. 

4. **A Touch of Humor**: Our assistant's wit echoes the minds it was nourished by. We sprinkled puns and Easter eggs into dialogues, like "Why do programmers prefer dark mode? Because light attracts bugs." ChatterSam developed a personality distinctly its own, from our whimsically acquired snippets.

## Unleashing the Final Creation

Testing and tweaking were Sam’s forte and soon enough, ChatterSam was ready to unleash upon the world. Running it through various quirky scenarios, our creation stood firm—unfazed by the tides of redundant inquiries and cheeky repartee. Essentially, what we’d crafted was beyond lines of code—it became a form of digital companionship.

It was high fives all around, laugh-out-loud moments shared, and a lingering realization that technology can feel as warm as a woolly blanket on a winter night if handled right. It was not merely an app but an exchange of dreams and delight between human and machine.

In this saga of discovery and learning that expelled us from routine into the realms of innovation and camaraderie, we found that our mistakes—and there were many—were the vessels that led us to breakthroughs. As we signed off from this adventure, we knew with each earnest line of code, in the many paths Jade Watson and Node.js shall take us, we shall sail forth – ready creatures of code who dare to whisper to AI.

And that, my friends, is the story we share—an odyssey we heartily recommend you undertake in your quest for understanding, wit, and above all, a dash of fun.