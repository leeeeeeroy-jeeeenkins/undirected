---
slug: creating-a-seamless-ci-cd-pipeline-with-terminus
title: Creating a Seamless CI CD Pipeline with Terminus
authors: [undirected]
---


# Creating a Seamless CI/CD Pipeline with Terminus

## Ah, the Quest for the Perfect Pipeline

It was one of those drizzly afternoons, the kind where the rain taps gently on the window like a shy neighbor asking for sugar. My buddy Mike and I were huddled over the glow of our laptops in a quaint little coffee shop that promised the world with its Wi-Fi but often delivered something more akin to a snail on a Sunday drive. Yet, here we were, determined to unravel the complexities of Continuous Integration and Continuous Deployment—CI/CD for those who prefer brevity—using the ever-mystical tool known as Terminus.

"Hey, remember when we thought setting up a CI/CD pipeline for our project would be a breeze?" Mike chuckled, taking a sip of his now-lukewarm coffee. I nodded, recalling our joint naïveté with a wistful fondness. It’s the kind of project that starts with optimism and ends with a lesson in humility. But amidst firmware failures and coffee spills, we discovered a tranquility in failure and a jubilant victory in each tiny success. And that—my dear reader—is precisely what paved the way for this step-by-step tale of CI/CD mastery we’re about to embark upon.

## Getting Acquainted with Terminus

Fast forward to the moment where we discovered Terminus—it was as if someone turned the lights on while we were still in metaphorical pajamas. For those not yet privy to its wonders, Terminus is a nifty command line tool designed for managing Pantheon websites. Now, I know what you're thinking—what does Pantheon, a hosting platform for sites, have to do with CI/CD? Quite a lot, as it turns out, when you’re neck-deep in a web development ecosystem. And there we were, navigating this labyrinth with our trusty guide, Terminus.

To get started, we needed to install it. Simple enough:

```bash
$ composer require pantheon-systems/terminus
```

But hold your horses, make sure you’ve got Composer on your machine first. Composer is like that elusive but necessary cord that connects your DJ set to the speakers at a party. No Composer, no music. (Or Terminus, in this case.)

## Integrating the Drums: Setting Up Version Control with GitHub

"I swear, if I have to reset this password one more time, I'm going to print it out and frame it," Mike muttered as he wrestled with his GitHub account. Indeed, no CI/CD journey is complete without traversing the realm of version control. Setting up GitHub was akin to learning the dance steps to a samba—a bit complicated but greatly satisfying once you catch the rhythm.

First, we created a repository for our project. Elevated it to the cloud, if you will.

```bash
$ git init
$ git remote add origin https://github.com/your-username/your-repo.git
```

Of course, replace `your-username` and `your-repo` with your actual details. Personalize your virtual stage.

## Orchestrating the Symphony: Creating the Pipeline

With Terminus and GitHub harmonized, it was time to weave our CI/CD pipeline, the very heart of our newfound technical symphony. We needed automation magic to make the steps of testing, building, and deploying hum in perfect unison.

We chose GitHub Actions—a versatile maestro—for this task.

Inside your repository, create a `.github/workflows` directory and an `action.yml` file to script your automation journey:

```yaml
name: CI/CD Pipeline

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Install Composer Dependencies
      run: composer install

    - name: Run Tests
      run: composer test

    - name: Deploy to Pantheon
      env:
        TERMINUS_TOKEN: ${{ secrets.TERMINUS_TOKEN }}
      run: |
        terminus auth:login --machine-token=$TERMINUS_TOKEN
        terminus env:deploy --site=your-site --env=dev
```

Here's where we faced our first "aha moment"—and potential facepalm—because everything seemed to either work flawlessly or fail miserably with no in-between.

## Navigating the Mists: Dealing with Environment Variables

"Isn’t it wild how coding reminds you of 20-step skincare routines?" I joked. Because managing environment variables was just that—a meticulous process requiring patience akin to waiting for an avocado to ripen.

GitHub offers a noble contraption called Secrets. Store your sensitive information, like tokens or API keys, there rather than leaving them strewn about your code like confetti.

Within your repository, navigate to `Settings > Secrets`, and add `TERMINUS_TOKEN`. It’s like locking your diary in a safe and hiding the key in a really obscure spot—a necessary intrusiveness to fend off unwanted guests.

## Symphonizing the Finale: Testing and Deployment

Our code was penned to paper—well, more like electrons to server, but you get the picture. Yet the true art lay in the performance, the build process, and the deployment. I can still picture Mike fidgeting with excitement as we awaited the green checkmark from our GitHub Actions page indicating success.

Testing isn't merely a task; it's a thrill. The build process ran our code through a series of trials—examining each function like a jeweler appraising a gem. And once every impediment was conquered, Terminus orchestrated the victorious deployment—a culmination of our efforts, akin to the conductor’s final baton flourish in a rousing overture.

Looking back, it's like running a marathon. There's sweat, strain, and perhaps a momentary desire to quit, but the finish line—and the cooler full of Gatorade—makes it worth every painstaking step.

## A Toast to Continuous Adventures

Our journey into the depths of CI/CD pipelines and Terminus unfolded like an epic tale with heroes, hurdles, and the glorious slaying of dull dragons known as debugging. We emerged more knowledgeable, somewhat caffeine-dependent, and infinitely inspired.

"Let's do this all over again for another project!" Mike exclaimed, proving that we are, at heart, gluttons for tech challenges. As we pack away our laptops and drain the last drop of coffee, we reflect on how technology is an art form. It’s never constant, always evolving, and continuously teaching.

Here's to the next chapter, whatever it may bring.