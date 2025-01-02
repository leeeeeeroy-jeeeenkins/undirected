---
slug: how-to-set-up-moodle-for-online-exams
title: How to Set Up Moodle for Online Exams
authors: [undirected]
---


# How to Set Up Moodle for Online Exams

There we were, my colleague Silvia and I, sitting in a slightly dusty room filled with the gentle hum of computer fans, determined to decipher the mysteries of Moodle like two adventurers bracing themselves to open a treasure map. "We got this," Silvia said, flashing me a grin as if she had just cracked some ancient code. And frankly, that moment - right there - was the seed from which this guide sprouted. Having stumbled through setting up our first online exam on Moodle, I figured, why not spare you the dust-stirring and head-scratching? So, grab a virtual coffee, and let's navigate Moodle together!

## Step 1: Setting Up Your Moodle Environment

Remember those old photographs of researchers buried beneath heaps of papers? That's how we felt before realizing that environment setup is our friend, not foe. First off, make sure Moodle is up and running on your server. If it's not, well… that's an adventure for another day. You might need an admin friend or some strong coffee.

### Step 1.1: Starting Up

To set this all in motion, log in as an admin or teacher (with course editing rights) - you know, with those fancy credentials. Click on the course where you want to add your exam. It’s like choosing a stage for your forthcoming masterpiece. 

* Click the `Turn editing on` button – usually at the top right - it's a small button that bears the weight of the world.
* Now, you'll see the magical `Add an activity or resource` link appear in each section of your course. It beckons you.

## Step 2: Create Your Exam Placeholder

Standing at the edge of creating an exam is a bit like staring at a blank canvas. Daunting but thrilling. You have so much potential to unleash!

### Step 2.1: Quiz Module

Selecting the `Quiz module` from the list of activities is our next play. It's like picking the right brush for your painting. Click `Add` with a touch of triumph.

* Give your quiz a name - something that screams "I'm important!" without being all caps and three exclamation points. 
* Write a compelling description so students know what they’re in for. "Prepare yourself, young Jedi" could work, but clarity is king.

### Step 2.2: Timing is Everything

Set the rules and timeline, a digital hourglass. Under the `Timing` section, click away.

* Enable `Open the quiz` and `Close the quiz` to specify when the magic happens.
* Set `Time limit` - the digital equivalent of a sand timer. Fifteen minutes, 120 minutes, choose wisely.

## Step 3: Layout and Questions

This part felt like decorating a room together – what's the flow, the vibe we want? 

### Step 3.1: Building the Structure

In the `Layout` section, decide how many questions per page - like chapters in a story.

* Choose a `New page` for every X questions. I'd suggest every one or two to keep it light and uncomplicated. 

### Step 3.2: The Heart of the Quiz

Questions are the blood, sweat, and pixels of this ordeal. Click on the `Edit quiz` button – your palette awaits.

* Add questions by clicking `Add` -> `+ a new question`. This is where you channel your inner trivia genius or sadistic riddler.
* Choose from question types – multiple choice, true/false, short answer, essay – like treasures in a pirate's chest.

#### Example of a Multiple Choice Question

```yaml
{
  "question_text": "The color of the sky is ___?",
  "type": "multiple_choice",
  "choices": ["Blue", "Red", "Orange"],
  "answer": "Blue"
}
```

Engage them with intrigue – or confound them. Your call.

## Step 4: Scoring and Attempts

It’s about fairness and chances. Like handing out candies.

### Step 4.1: Grades and Attempts

In the `Grade` section, decide on the scoring method and attempt limits. Choices, always choices.

* Set `Grade to pass`. Maybe aim for a B-minus vibes, not A++ massive stress.
* `Attempts allowed` - is it one kick at the can or a friendly best-of-three?

### Step 4.2: Review Options

Take a cup of feelings about feedback. When can they see results? Adjust `Review options` if you want to shield and unveil truths methodically or instantaneously. 

## Step 5: Addressing Accessibility

For some reason, this part reminds me of my grandmother saving seats at family gatherings. Make sure everyone is included.

### Step 5.1: User Overrides and Group Overrides

Under `User overrides` or `Group overrides`, you find the control panel that lets you accommodate special timings and settings for individuals or groups who need it.

* This is our chance to be fair, allowing extensions or alterations for those whose constraints deserve bending.

## Step 6: Test and Troubleshoot

Now what feels like the most crucial trial - our debuts require a faithful practice run, pre-show tweaks.

### Step 6.1: Pilot Runs

Conduct a dry run - it's like auditioning cooking before a feast. Test the quiz yourself or with a small group to ensure everything functions as it should.

* Look out for questions that don’t load, time settings that rebel, or grades that don't compute.

### Step 6.2: Getting Feedback

Once the initial kinks get ironed, solicit feedback from test-takers, and wear your thickest skin. They’ll unearth issues we never dreamed of. 

## Step 7: Go Live and Monitor

Launching an exam hurls you into dual realms of exhilaration and anticipatory dread. How will folks fare in this world you built?

### Step 7.1: Opening Day

With regulations checked off and enthusiasm somewhat contained, say a silent "good luck" and unleash the quiz to students. This is your big reveal!

### Step 7.2: Real-time Monitoring

Keep a watchful eye, like a benevolent guardian. Moodle's monitoring tools can highlight irregular activity during the live exam - pop under `Quiz administration` -> `Logs` if anything smells fishy.

## Troubleshooting Common Problems

"Oh no, something went wrong!" echoes in our heads when the tech doesn't bode well. Breathe in, we’ve got this.

### Common Issue #1: Quiz Not Opening

If your quiz stubbornly blocks entry, check the quiz availability settings under `Timing`. Also, make sure participants have the appropriate permissions.

### Common Issue #2: Question Visibility

If questions evaporate into the ether for some reason, revisit the layout and question bank to ensure each query is properly linked.

## A Sweet Farewell

And there we have it, dear pioneers of digital assessment realms. From cautious beginnings alongside Silvia's hopeful grin to now, we’ve turned the whirring mystery into a well-oiled exam machine. Reflect on the journey, take pride in vanquishing what once loomed as monsters. Pat yourselves on the back, celebrate small triumphs - but ignore the dust we’ve stirred. Until next time, keep exploring, keep learning.

So, how’d we do? Found any lingering puzzle pieces I forgot to address, or is there a Moodle story you’re bursting to share? Let’s keep this conversation rolling in the comments below. We’d love to hear from you.