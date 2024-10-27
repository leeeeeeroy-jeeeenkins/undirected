---
slug: how-to-create-scripts-in-terminus-for-automation
title: How to Create Scripts in Terminus for Automation
authors: [undirected]
---


# How to Create Scripts in Terminus for Automation

You know, the moment I first realized how much of my life was slipping away because of mundane, repetitive tasks, I was staring at an endless spreadsheet. My fingers felt like they were stuck on autopilot, tapping the same keys over and over again, like some kind of monotonous symphony. That's when I decided it was time for a change. I had heard whispers of this mystical thing called "automation"—a sort of digital magic that could free us from the shackles of repetitive work. So, down the rabbit hole I went, diving into the world of scripting in Terminus.

### Finding the Magic in Automation

When we talk about automation, our collective minds might drift toward images of robots taking over the world—or at least making our morning coffee. But, rest assured, what we're dealing with here is much kinder and way less intimidating. Terminus, the command-line interface tool built by Pantheon, can help us weave some of this magic, making our day-to-day tasks quicker and more efficient, kind of like the difference between walking uphill with a piano strapped to your back versus gracefully soaring on an escalator.

Terminus itself is like that old reliable toolkit handed down through generations, complete with lots of mysterious gadgets and gizmos you may have only dreamed about. What if we could add our own customized wrenches and hammers—or in this case, scripts—to this toolkit? Well, my friends, that's exactly what we're going to do.

### Step 1: Prepping Our Magic Workshop

First things first: if we're going to run scripts in Terminus, we'll need the esteemed Terminus itself. Installing Terminus is much like installing a new sense of control over your digital tasks. If you don't have it yet, you can get started by following these straightforward steps:

1. Head over to [Pantheon's official documentation](https://pantheon.io/docs/terminus/install) and pick up the latest version of Terminus suited for your machine.
2. Follow the installation steps specific to your operating system. They've done a pretty stellar job of breaking it down like a classic DIY manual, so fear not.
3. Now, open your Terminal or Command Prompt. We want to make sure that Terminus is all cozy in your system. Run:

   ```bash
   terminus --version
   ```

   If it throws back the version number without complaining, congratulations! You've officially laid down the first brick in constructing your automation empire.

### Step 2: Learning to Speak Our New Language

Next up, and arguably more thrilling, is getting the hang of command-line scripting. It's like learning to speak a secret language where each command holds the power to transform chaos into order. Let's explore a simple Terminus command:

```bash
terminus site:list
```

Running this command, we ask Terminus to neatly lay out a current list of sites for us. Think of it as your personal butler, kindly updating you on what's in the digital pantry.

Now, I understand that the command line can seem like a daunting dance of symbols and letters, but trust me, it's more like learning a catchy rhythm—you just need a bit of patience to get it stuck in your head.

### Step 3: Drawing Up Our First Script 

Think back to that moment when you finally learned how to ride a bike—there was freedom, maybe a few wobbles, but ultimately, joy. That's what writing your first script feels like. Let's ease into it with a script that backs up all your sites on Pantheon. It's a simple start, but it's profound in its utility.

1. Fire up your favorite text editor. This could be anything from VS Code to something classic like vim or nano.
2. Create a new file called `backup_sites.sh`—naming conventions and an extension are what make it feel official.
3. Type in the following script:

   ```bash
   #!/bin/bash

   sites=$(terminus site:list --format=list --field=ids)

   for site in $sites; do
       echo "Backing up site: $site"
       terminus backup:create $site --element=all
   done
   ```

4. Save the file and close your editor.

Looking at our script, you might think it's holding a bit of wizardry inside. What we've got is a loop—it’s our script going through each site and telling it to back itself up. That’s automation casting its spell. The `#!/bin/bash` at the beginning? That's our script announcer, telling the system we're in for some good, clean shell scripting fun.

### Step 4: The Big Show: Running Your Script

So, you've drawn your plans and assembled everything to create automation magic. Now it’s showtime. Let’s bring it all together and run our script. Much like watching bread rise in the oven, running your script is where you witness the magic happen.
 
1. Before running, make sure our script is executable. From your terminal, navigate to where your `backup_sites.sh` file is saved.
2. Run this command to make it executable:

   ```bash
   chmod +x backup_sites.sh
   ```

3. Last, it’s time to execute. Run:

   ```bash
   ./backup_sites.sh
   ```

As the script runs, it's as though you've flipped a switch, and everything bursts into life. Each echo in the terminal is like a beat of the drum, affirming the script's actions, giving a small salute as each site is safely packed away in a backup.

### The Lessons Learned and the Road Ahead

As I watched my script do what I used to spend hours doing, I couldn't help but marvel at humans' ingenuity—one moment we're bogged down with tasks, and the next, we're befriending tools to do the heavy lifting for us. Automation with Terminus isn't just about efficiency; it's about empowerment. It's like having a dependable friend who's ready to help at a moment's notice, someone who takes care of every little detail that used to stress us out.

There's more exploring to do, so many more scripts to write, always evolving. Just like us. There's joy in knowing that with scripting, small improvements lead to greater happiness, not just in minutes saved, but in finding new possibilities in every task. Automate what you can, share it with others, and let’s continue building together.

So, here's to more time spent on projects that matter, to fewer mundane routines. After all, the remainder of our journey through the digital realm is all about discovery and invention. We’re free to create, to imagine—to let automation take over the echoes and frees us for the symphonies.

*Quite the adventure lies ahead—won't you join us?*