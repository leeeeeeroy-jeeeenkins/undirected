---
slug: how-to-set-up-secure-shell-access-in-terminus
title: How to Set Up Secure Shell Access in Terminus
authors: [undirected]
---


# How to Set Up Secure Shell Access in Terminus

It was last Tuesday when my cat decided to reprogram my computer with an unexpected keyboard walk. As I revived my screen – thanks to the nine lives of ‘undo’ – a thought hit me like a lightning bolt in a summer storm: wouldn’t it be splendid if we, just a couple of curious souls seeking tech enlightenment, knew exactly how to set up Secure Shell (SSH) access in Terminus? Think of the time saved, the frustration avoided! So I decided to delve into this universe, herding the cats of technology and writing it all down, like an adventurer with tales of dragon-slaying adventures, but with fewer mythical beasts. (Although, network glitches might argue otherwise.)

## Setting the Stage

We've all been there, tangled in the webs of wires and wireless connections, yearning for some simplicity – like discovering a new favorite ice cream flavor that doesn't require a complex ordering ritual. Terminus, our trusty Terminus, is a fabulous tool that weaves together a beautiful SSH tapestry. So, let's hook our sail to this sturdy vessel and meander through the process of getting SSH up and running in Terminus, as smoothly as a cat landing on its feet.

### Step 1: Juicing Up the Engine

Now, my first brush with SSH was like learning to ride a bike with one eye closed. There was anticipation, excitement, and a lot of wobbles. So let's start by making sure our dashboard is ready. Fire up your Terminus app. Are you greeted by a warm, friendly interface? Perfect. If there’s an update lingering around like a party guest who’s overstayed, make sure to install it – we don’t need any outdated sprites taking us on detours.

Once we're updated and ready, open the app. Ah, the sweet digital aroma of possibilities.

### Step 2: Profiling Our Path

Creating a new profile in Terminus is akin to laying out your outfit before a big day. We want it sharp, functional, and maybe with a splash of color if we're daring. To start, navigate to the app's Profiles section. In this little corner, you’re the maestro, orchestrating a symphony of connectivity. Select the ‘Add’ or '+' button – depending on your version's vocabulary – which is usually in plain sight. Go on, click it bravely.

Now, enter the new profile details. If our computer is in technicolor jeans, think of these fields as the quirky belt that ties it all together. Add a name that's easy to remember; this is for your future self who might be pre-coffee and a tad forgetful.

### Step 3: Choosing the Right Instruments

Next, guide your eyes to the ‘Host’ field. You know how some things just sound right? Like the crispness of falling leaves underfoot. Here, you need to input the hostname or IP address of the server you want to access. It’s like dialing a friend’s number into an old landline – analog charm, digital precision.

In the port field, we keep it classic; '22' usually does the trick – it’s the SSH default dance number. Feel free to jazz it up if your server prefers a different shuffle.

### Step 4: The Balancing Act of Authentication

Now we reach one of those crucial crossroads – like choosing between two beloved desserts. Do we go password or key authentication? While both have their merits – akin to chocolate and vanilla – our focus today is on the robust security of key authentication. So, let’s generate that SSH key with the flair of a magician pulling rabbits from a hat.

Open your terminal. With the grace of a swan, although perhaps just as klutzy, type:

```bash
ssh-keygen
```

This command will lead you through a delicate dance of creating a private-public key pair. Tap ‘Enter’ to accept default locations, and add a passphrase – consider it the secret spice in your grandmother’s stew recipe.

### Step 5: The Trust Bridge

Our SSH key is now an artifact of beauty, like a newly discovered constellation waiting to be named. We just need to connect the dots. The public key – our galaxy map – needs to be added to the server's `.ssh/authorized_keys` file.

Use a command like:

```bash
ssh-copy-id user@host
```

Replace ‘user’ and ‘host’ with, you guessed it, your username and server address. This command is the diligent postperson, delivering your SSH key to the right doorstep – minus the holiday fudge.

### Step 6: The Grand Test

Grab your ceremonial hat – or just a coffee, really. It's time to connect. In Terminus, return to your profile and hit ‘connect’. As the connection sparkles to life – ideally sans the spinning wheel of doom – you should find yourself logged in with applause from invisible tech muses.

And there you have it. Now we’re not just surviving the tempestuous seas of SSH and Terminus, but thriving upon them like seasoned explorers of code.

## Conclusion: The Afterglow

With this know-how, we've turned SSH setup from a cryptic trial into an inviting adventure – not unlike winning a treasure hunt without losing a shoe. Remember, the key lies in practice and perception. Even if fluffy paws revisit your keyboard, you'll be ready. We'll face the tech future with an open heart, sprinkled with just a dash of mirth.