---
slug: how-to-use-docker-with-terminus-for-testing-environments
title: How to Use Docker with Terminus for Testing Environments
authors: [undirected]
---


# How to Use Docker with Terminus for Testing Environments

Once upon a time, in the bustling heart of a coffee shop infused with the aroma of freshly ground beans, we found ourselves seated across from an old friend, Alex—a rather brilliant, slightly sarcastic dev who always seemed to have a solution up his sleeve. It was him who introduced us to an exciting intersection of technology that would soon become indispensable: using Docker with Terminus for setting up vibrant testing environments. As he spun tales of streamlined processes and nimble deployments, we couldn’t help but lean in, intrigued, eager to unravel the mysteries of this powerful duo. It sounded like magic, but as we discovered, it was a joyous marriage of practicality and innovation.

## Setting Up: The Prelude

Our story begins, as all good ones do, with some groundwork. Before diving headlong into Docker and Terminus, there's a little preparatory handiwork to be done. First, we install Docker. If you’re anything like us, you already have it installed—but console cowboys among us, here’s a quick jog through the basics. Download Docker Desktop for your OS from the Docker website. Install it following your system prompts, and voilà, Docker's cheerful little whale icon joins the party.

Then there’s Terminus—the command-line interface (CLI) for Pantheon—which requires its fair share of setup. "Python? PHP? No, my friend, it's a delightful little tool that makes managing Pantheon sites a breeze," Alex had assured us, with a sip of his double espresso. We nodded, both bewildered and charmed.

Let’s walk the plank and get Terminus cozy on our machine. Fire up your terminal, and use Homebrew for a swift installation:

```bash
brew install pantheon-systems/external/terminus
```

Once that’s breezed through, don’t forget to authenticate:

```bash
terminus auth:login
```

You’ll need your Pantheon credentials—like a secret password to a treasure chest full of web-Heiresses.

## Docker Meets Terminus: The Plot Thickens

With our trusty tools at our command, like knights riding into battle, we’re prepared to create. Now comes the artful weaving of Docker and Terminus for our testing spectacles. It starts with something we noticed Alex doing after he'd downed his third cup of joe—it involved wrangling containers as though they were wild stallions.

We create a Pantheon environment snapshot - a version of your site preserved in amber - ready for a rendezvous with Docker. The `terminus backup:create` command freezes this moment, prudent insurance when dealing with the unforeseeable:

```bash
terminus backup:create my-site.dev --element=database --keep-for=30
```

(Our poor friend Alex once lost an afternoon's work for skimping on this step. Don’t be Alex.)

## Crafting The Docker Image: What’s in Pandora’s Box?

With backups safe and Terminus logged in, we turn our crafty attention to Docker. You’ll want to create a Docker image—a base from which your container sprints forth. Think of an image as a blueprint, a chef’s secret recipe. This involves crafting a `Dockerfile`. Oh, the thrill!

Here's a simple template to start:

```Dockerfile
FROM php:7.4-cli
WORKDIR /app
COPY . /app
RUN docker-php-ext-install pdo pdo_mysql
CMD ["php", "artisan", "serve"]
```

Each instruction layers over the previous like pastry bags building a towering croquembouche.

## Containerizing Our Testing Environment: Dancing with Containers

Now, for the exciting part. We’re assembling our container, the chariot to our image’s stallion. We’ll use the `docker-compose.yml` file to define services. Think of it like setting up dominos. Align assignment after assignment until unstoppable motion.

This is where we set the mood, the atmosphere in which our application thrives.

```yaml
version: '3.8'

services:
  web:
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "8000:80"
    volumes:
      - ./:/var/www/html
```

Running `docker-compose up --build` summons your container as if conjured by spell. Watch as logs spring to life.

## Testing with Terminus: Where Rubber Meets The Road

And now, the pièce de résistance. This is where testing environments, terminus magic, and sharp-eyed monitoring meet in glorious harmony. With your Docker container buzzing along, logs zooming past like subway trains, we return to Terminus for command-line fireworks.

Want to import your Pantheon database? We ask Terminus with a quiet clickity clack:

```bash
terminus backup:get my-site.dev --to=local.sql.gz
gunzip local.sql.gz
docker exec -i <container_id> mysql -u root -ppassword < database < local.sql
```

Always ensure your local Docker instance feels pampered and refreshed using `docker-compose down` followed by a `docker-compose up`—almost like taking a leisurely Sunday stroll post a savory brunch.

## A Reflective Epilogue

As the afterglow of successful testing environments illuminates our development path, we return to the present—grateful for experiences and a touch of wizardry gained with Docker and Terminus. For all its quirks and causes of befuddlement, it's terribly satisfying to tame servers and orchestrate containers with nothing more than a keyboard and a glint in our eyes. Alex, in all his caffeine-fueled wisdom, showed us a glimpse of this wonderland, but it’s our own explorative spirit that sustains the journey.

Discovering Docker with Terminus is like finding the perfect melody for a bustling city, the right filter for a snapshot in time—we build, break, learn, and kindle our passion for coding anew. Spurred onward, sharing these sparks of insight, let’s remember the fun, the magic, and most importantly, the first slurp of coffee that started it all. Here’s to new adventures and grand tests ahead—may there be many backups and airtight containers along the way. Cheers!