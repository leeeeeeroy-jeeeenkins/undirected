---
slug: automating-backups-using-terminus-and-scripting
title: Automating Backups Using Terminus and Scripting
authors: [undirected]
---


# Automating Backups Using Terminus and Scripting: A Joyful Journey into Efficiency

Have you ever had one of those days where the universe gives you a clue—one of those cosmic hints that maybe, just maybe, relying on human memory for critical tasks might not be the best strategy? Picture this: I was sipping coffee, basking in the lazy warmth of a Sunday morning when my phone buzzed. It was Chris, our tech-whiz pal with the unfortunate title of "The Designated Fixer of Things Gone Wrong." His message simply read, "Hey, did anyone remember to back up the sites last night?" Panic ensued. You see, we had a pretty gnarly experience with a server crash not too long ago, and let's just say, scouring the digital wreckage was not my idea of a great time.

From this chaos bloomed our pursuit of automating backups—enter Terminus and a sprinkle of scripting magic. Backups needed to be as reliable as morning coffee and as automatic as the sunrise. Chris, fueled by the combined forces of caffeine and determination, shared his plan to prevent us from ever feeling the icy grip of backup-related dread again.

## Unraveling the Mystique of Terminus

As often happens during our nerdy brainstorming sessions, Terminus came up. Not to be confused with a Terminator spin-off, Terminus is the mighty command-line interface for Pantheon, wielded with the caution and respect one might afford an ancient, wise wizard. If your web life resides on Pantheon, Terminus is your go-to for command-line dancing. It was like finding the perfect pen for writing backup poetry—though we're not really poets, as you'll see shortly.

So, the journey kicked off with installing Terminus. We needed to summon it onto our local machine. The installation was simple enough (Chris could install it with both eyes shut). Pop open the terminal and run:

```sh
composer require pantheon-systems/terminus
```

You'd think that was the hard part, but no—life likes to surprise us.

With Terminus successfully embedded into our digital world, it needed credentials. Like a nightclub bouncer, it wouldn't let you in without a proper ID. Chris excitingly exclaimed, "Create a machine token, and we'll run this place in no time!" We hopped onto the Pantheon dashboard, navigated with the grace of Indiana Jones in a digital museum, and conjured our magic credentials.

## Scripting - The Art of Making Machines Work for You

The most satisfying part of our journey was the discovery of scripting, where we humans made machines do our bidding with the eloquence of a Shakespeare sonnet—wait, maybe that's overselling it. At any rate, we glided smoothly with bash scripting.

We opened our text editor, fingers gingerly dancing over the keys like musicians coaxing enchanting melodies. And we wrote, against all odds, a script like this:

```sh
#!/bin/bash
sites=(site1 site2 site3)  # The Pantheon sites we need to backup

for site in "${sites[@]}"; do
  terminus backup:create "$site".dev
  echo "Backup for $site completed."
done

echo "All backups are done!"
```

We saved it, like a cherished letter from an old friend—`backup.sh` was its name, an unassuming guardian of nostalgic peace of mind. This script, once scheduled, would steel itself to run automatically, like a responsible adult we hoped to be. We entered crontab, a mysterious realm where time travelers dwell, and crafted our time spell:

```sh
0 2 * * * /path/to/backup.sh >> /path/to/backup_log.txt 2>&1
```

Chris looked particularly triumphant, like he had just pulled a backup rabbit out of a digital hat. My excitement brimmed as I envisioned those backup schedules—like unspoken promises we intended to keep forever. 

## Connecting the Dots with Automation

Our intention was to live free from the chains of manual backups—a promise of effortless peace, thanks to our duo of Terminus and scripting. After verifying the backups through the Pantheon dashboard (because trust but verify sounds like solid advice), we marched into the land of automation. Chris, always the optimist, suggested we keep an eye out for clever logs or notifications just in case our digital helpers ever need a nudge.

But here’s the secret sauce: use third-party services like Slack or email APIs, let them shout from the rooftops, "Backups are safe!" Trust me, there's immeasurable joy in knowing that our metaphorical house is in order and secure.

## Reflection: The Warm Glow of Backups Done Right

Years from now, when the sun sets over a valley of forgotten digital disasters—likely hastened by either a storm or a grand new technology failed fantasy—our little backup automation journey will shine like a beacon in history's annals. 

As we now look back on our achievements (modest as they may seem), we're cradled in the knowledge that we've given our dearly beloved websites the security blanket of automated backups—all thanks to a small blend of Terminus and scripting. They are beloved to us, these digital creations. And this journey shared with Chris has reaffirmed that, yes, even the smallest of processes hold great value.

Remember the small Sunday morning mishap that set this ball rolling? Chris and I often laugh about it now, as we reminisce about the digital dragons we’ve slain and the cups of coffee fuel that ran our adventures. You know, with the right mix of tools and a little joy, automating tedious tasks can indeed be a heartwarming experience.

So let's raise a mug of something caffeine-infused—cheers to backups, automation, and the delightful symphony of a Sunday morning well-spent!