---
slug: how-to-create-custom-scripts-in-terminus
title: How to Create Custom Scripts in Terminus
authors: [undirected]
---


# How to Create Custom Scripts in Terminus

Ah, Terminus. Just saying the name sends me back to that little incident with the pizza delivery. I was neck-deep in a knot of endless digital wires, trying to coax a misbehaving server into singing the song of its people, when the smell of cheese and oregano wafted through the air. The delivery guy—bless his pepperoni-scented soul—had shown up just when I hit "Run" on a hastily drafted script. The screen lit up in a cascade of promises finally kept. That simple script—less a code, more a whispered prayer—had finally untangled my vile web of errors. And there, between bites of slightly cold pizza and hints of refactored variables, a thought dawned. Why not share the magic of crafting these digital spells with others? And so, here we are, in the world of custom scripts and Terminus, arm in arm, ready to embrace the chaos and glory of code.

## Discovering Terminus

If you haven't yet danced with the symphony that is Terminus, let us whisper its wonders to you. Terminus is magical, like something out of a tech wizard's toolbox—a command-line interface that makes Pantheon's hosting platform bow to our will. It allows us to manage Drupal and WordPress sites with a flick of a script, a dash of a command, a touch of genius that only we possess (and by 'we,' I mean anyone who bothers to read the documentation).

Let's step back to that unassuming evening. Terminus stood there, unruffled, ready to be molded by the gentle caress of our keyboard fingers. We loaded it up, bright and full of promise, on our trusty workstation. Oh, Terminus, what adventures we embarked upon together! And you, dear reader, can join us on these ventures of script-writing glory with just a little guidance.

## Setting Up Our Coding Scene

Do you ever get that new project jitters, like the anticipation before opening a new book? It’s like that first sip of coffee on a cold morning. First, we need to set up our environment for crafting these digital lines of wonder. For this, let’s embark on a short journey to our computers—or whatever coding device is nearest.

### Step 1: Install Terminus

Our first stop is ensuring we have Terminus installed. Check, double-check—triple if you’re feeling meticulous—whether you’ve got Terminus resting comfortably in your command line. If it’s your first rodeo, you’ll want to gallop over to [Terminus's installation guide](https://pantheon.io/docs/terminus/install). Follow along with caution, installing via Homebrew, npm, or Composer. Or, less thrillingly, you can download an executable file and be done with it. But where’s the fun in that?

### Step 2: Authentication

Now that Terminus is nestled in our CLI, cuddling up against the lines of code, we need to let it know we’re best pals. At the forefront, the `terminus auth:login` command beckons. Enter your Pantheon credentials with pride, and feel the authoritative acknowledgement of authentication.

```bash
terminus auth:login
```

With that, we have the keys to the kingdom—a kingdom of limitless site management possibilities. Feeling the power yet? Just wait.

## Dreaming Up Our Script

**Scene One**: An empty text editor sits before us, waiting for its canvas to be filled. We take a breath, letting ideas simmer and stew. What do we want? What does our heart yearn for in this script? Ah! To automate backing up our website. Simple, elegant, save us some Saturday afternoon sanity.

In my case, the sparkle of an idea twinkles: automatic backups of our beloved site. Something simple, something sweet.

### Step 3: Begin the Script

Open your favored text editor—embrace your inner artist, choosing your brush. Be it Visual Studio Code, Sublime, or vim—yes, even vim, if you're a masochist like some of us. Wherever you choose, create a new file, perhaps lovingly named `backup-script.sh`.

Here begins our script, its mantra concisely starting with the shebang magic incantation to declare this as a bash script:

```bash
#!/bin/bash
```

Ah, the simple beauty of it. The shebang demands our script be taken seriously—it’s how Unix-like operating systems know to execute the script with the bash shell.

## Our First Command

I could almost hear the distant echoes of my past scripting flubs. The `terminus auth:login` became intimately familiar to me, its aura like an old friend. Let's feed that into our script to ensure it knows who we are:

```bash
# Authenticate with Terminus
terminus auth:login --machine-token=<YOUR_MACHINE_TOKEN>
```

Replace `<YOUR_MACHINE_TOKEN>` with your actual machine token—don’t fumble around with the wrong keys. 

### Step 4: The Actual Task

Now, with the boldness of a night owl hitting "next episode," let's get to the meat of what we’ve come for: backing up the site. Forged in the fires of insomniac coding sessions, the following lines work to backup our site:

```bash
# Ensure we’re authenticated before running Terminus commands
if ! terminus auth:whoami &> /dev/null
then
    echo "Not authenticated; please check your credentials."
    exit 1
fi

# Site and environment variables
SITE_NAME=my-awesome-site
ENV_NAME=dev

# Create backup
terminus backup:create $SITE_NAME.$ENV_NAME
```

Ah, look at what we've done! We’ve taken a leap that’s sure to echo in our sleeping hours. By declaring variables `SITE_NAME` and `ENV_NAME`, we can reuse these handcrafted lines, propagated across any site we choose.

## Embracing Error

The first time I ran one of my scripts, I must’ve made every mistake known to human and cyber history. But remember, dear reader, mistakes are but concertos in disguise, waiting to be mastered.

### Step 5: Divide and Conquer the Debug

Run your script with the eyes of a hawk, ready to pounce on any trouble. If you've sprinkled wrong values or forgotten a closing brace, it’s time to play detective. Announce your success or failure, and the computer shall obey (more like politely hinting through error messages):

```bash
if [ $? -eq 0 ]; then
    echo "Backup succeeded!"
else
    echo "Backup failed. Check the logs for more details."
fi
```

Remember, with scripting, as with pizza delivery, timing is everything. There’s no shame in taking a step back, having a slice, and returning with a fresh perspective and a full stomach.

## Retrospect and Celebration

Reflecting upon our achievement, I keep going back to that pizza night. There’s something poetic about it, the way a simple script changed everything. We, too, have journeyed from scriptless vacancy to a thriving world of site management. With Terminus and a dash of creativity, we've written more than code. We've written our own story, with plot twists involving troubleshooting, and character developments made of punctual syntax.

In the end, whether we script out of necessity, curiosity, or just sheer love, remember our strength lies not just in the code we write, but in the joy we find in it. As we save our scripts and close the chapter on this adventure, let us look forward to the next one—a fresh cup of coffee, a new site to manage, and another script to craft, each line a testament to our little victories.