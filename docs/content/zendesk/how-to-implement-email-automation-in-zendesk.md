---
slug: how-to-implement-email-automation-in-zendesk
title: How to Implement Email Automation in Zendesk
authors: [undirected]
---


# How to Implement Email Automation in Zendesk

So there we were, knee-deep in customer support hell and sipping, relentlessly I might add, some questionable office coffee. I, along with my colleague Molly, noticed our new Zendesk dashboard staring back at us like a bewildered toddler, and it hit us—there was no way we could keep this up manually. I nudged her, whispering conspiratorially, as if imparting some great cosmic truth: "Email automation—it's time." 

That revelation took us on a wild journey—a journey paved with curiosity, a dollop of confusion, and remarkable discoveries that I’m now thrilled to share with you. Here’s how we became conquerors of chaos through email automation in Zendesk. 

## The Reckoning: Realizing Automation is Your Saviour

Our inbox looked like it had thrown a raucous party and forgotten to invite us. Every day was like trying to tame a hydra—a classic case of email overload. Molly and I finally decided: enough was enough. We needed a plan; automation was our unsuspecting hero. 

1. **Identify Repeated Tasks:** 
   - We jotted down all those tasks that made us roll our eyes every time we hit send. You know the type—confirmation emails, ticket responses, status updates. 

2. **Define Your Goals:** 
   - "What do we want from this automation?" I mused, half to myself. Molly quickly added, "Efficiency without losing our last nerve." Yep, that’s us, shooting for the stars.

Now, with these initial steps, we were ready to up the ante and explore email automation in Zendesk.

## Step 1: Getting Cozy with Triggers

A pivotal moment came when Molly discovered Triggers, those magical behind-the-scenes puppeteers. These are not spooky at all, really. They’re merely the brains behind our responsive email system, sending messages based on specific events.

1. **Navigate to Triggers:**
   - Go to the Admin Center, feeling like a tech wizard, and select *"Business Rules"*. Then, click *"Triggers"*. 

2. **Create a New Trigger:**
   - We clicked on *"Add Trigger"*—easy peasy. A simple name and description later, we took our first step into automation nirvana. 

3. **Define Conditions and Actions:**
   - We brainstormed conditions that would automatically spring into action. Like when a ticket status changes or a specific tag is added (oh, it felt almost Shakespearean in its simple complexity). Choose from actions like sending notifications and updating the ticket status.

Code snippet heaven:

```ruby
if ticket.status == 'New'
  notification.send('Email Subject', 'Dear Customer, your ticket is now in progress.')
end
```

## Step 2: Turning Macros into Our Handy Sidekicks

With triggers working their magic, it was time to summon Macros. These beauties allowed us to respond with pre-styled emails more fluently than I could ask, “Who drank all the coffee?”

1. **Navigate to Macros:**
   - In Zendesk, we gleefully clicked through to *"Admin Center"*, then *"Business Rules"*, and joyously landed on *"Macros"*.

2. **Create a Macro:**
   - We hit that *"Add Macro"* button—feels like unleashing superpowers, truly—and crafted our mystique-like responses.

3. **Craft and Assign the Macro:**
   - Molly and I, armed with our newfound knowledge, wrote clear, concise messages, complete with fill-ins for personal touches because we wanted our customers to feel the warmth through the keyboard.

Example of macro magic:

```json
{
  "macros": [
    {
      "title": "Welcome Email",
      "actions": [
        {"field": "status", "value": "open"},
        {"field": "subject", "value": "Welcome to Our Support"}
      ]
    }
  ]
}
```

## Step 3: Scheduling like Superheroes with Automations

By now, our emails were practically managing themselves. Yet, we needed to tie up the loose ends—follow-ups with the grace of a ballerina. Enter Automations.

1. **Navigate to Automations:**
   - Also nestled under *"Business Rules"* in the Admin Center. We were officially residents now, setting automations to work on ticket timelines.

2. **Create Automations:**
   - Automations, as it turns out, are splendid for those repetitive chores. We crafted a series of time-based actions like a perfectly orchestrated symphony. It was poetry in motion—literally.

3. **Set Conditions and Actions:**
   - We continued in our whimsical exploration, defining automations like a mad-lib, except infinitely more useful, ensuring tickets that wallow in neglect for too long get a little nudge.

Automation in code:

```yaml
when: 
  all: 
    - 
      left: field
      operator: greater_than
      right: 24h
then:
  notify: 
    email: "Time is ticking"
  message: "Dear Agent, please check on pending tickets."
```

## Step 4: Testing—Making Sure We Don't Break the Internet

Molly, the ever-pragmatic, wisely suggested a trial run. We didn't want our automations staging a coup. Testing and refining became our recurring ritual—like trying on hats until we found the perfect one.

1. **Test with Sample Data:**
   - We ran scenarios like ecstatic scientists, experimenting feverishly but ensuring our recipients weren’t real people, just test accounts. 

2. **Adjust and Refine:**
   - Feedback—thank you, imaginary customers—helped us refine and improve until we felt like the benevolent overlords of an automated kingdom.

## Final Thoughts: Making Friends with Automation

It’s been an enlightening journey since our chaotic email days. Automation didn't just save time—it renewed our sanity. Reflecting on our experience now feels like reliving a romcom with Zendesk playing the quirky matchmaker. 

Whether you’re drowning in emails or just sipping a lukewarm coffee contemplating your next big move, remember: embrace the waltz of automation. Embrace Zendesk. Dance deftly into productivity; after all, we're here to make technology less of a foe and more of a delightful ally.
```
