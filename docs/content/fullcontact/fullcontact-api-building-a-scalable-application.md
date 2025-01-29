---
slug: fullcontact-api-building-a-scalable-application
title: FullContact API Building a Scalable Application
authors: [undirected]
---


# FullContact API: Building a Scalable Application

Somewhere between my coffee running out and the realization that my cat had decisively commandeered my keyboard — again — I had an epiphany. Could we, mere digital artisans, construct something as grand and complex as a scalable application using the FullContact API, without losing our sanity or compiling a Vesuvius of spaghetti code? Spoiler alert: We can. Stick around if this notion tickles your neurons.

## A Journey of Hemmingway-Esque Proportions

It was a gray Tuesday morning — though, in my memory, it always feels rather sepia-toned. I found myself knee-deep in code, Kenneth in the adjacent chair humming tunelessly to a song only he knew. The kind of morning where the clouds were cranky and so was my codebase, which seemed determined to defy any form of scaling. I suddenly realized we had only print statements and prophecies driving our debugging process. We needed to refactor, rethink, and resurrect our approach with something sturdy but flexible — enter the FullContact API.

### Setting the Scene: Getting to Know FullContact

We begin at the beginning. FullContact offers a comprehensive set of tools to manage people data, perfect for those of us with aspirations bigger than our skillset. Think of it as the Swiss Army knife of APIs for contact management. Armed with this tool, we were ready to face anything the universe — or Kenneth’s unpredictable playlist — could throw at us.

### First Steps: Grabbing the API Keys

Ah, the sacred key. Before we dive headfirst into the code, let's grab our lifeline: the API key. In your FullContact account, navigate to your dashboard. Here, nestled like a prized gem, lies your API key. Copy it delicately, as if it might shatter if handled too roughly.

```bash
# Environment Variables
export FULLCONTACT_API_KEY='your-api-key-here'
```

Pro tip: never, ever leave this precious gem lying around in your source code — guard it like the last cookie in the jar. Moving on.

### Building the Foundation: A Skeleton App

Once upon a coffee, the idea dawned upon us to first assemble a mere skeleton of an application. A bare-bones Python script is needed to help us commune with the API. With a flick of the terminal, we create a new directory and venture forth.

```bash
mkdir fullcontact_project
cd fullcontact_project
touch app.py
```

With app.py created, we can commence our adventure. Breathe life into this shell with a binding spell — or rather, by launching our favorite code editor (we chose VS Code, for its fastidious charm and insightful linting). Install the necessary library:

```bash
pip install requests
```

### A Dash of Code: Our First API Call

Honestly, if making API calls feels like casting spells, then `requests` is our trusty wand. Let’s conjure a simple API call to fetch contact data. Open `app.py` and bless it with this invocation:

```python
import os
import requests

API_KEY = os.getenv('FULLCONTACT_API_KEY')  # Remember that gem you tucked away?

def get_contact_info(email):
    url = f"https://api.fullcontact.com/v3/person.enrich"
    headers = {
        'Authorization': f'Bearer {API_KEY}',
        'Content-Type': 'application/json'
    }
    payload = {"email": email}
    
    response = requests.post(url, headers=headers, json=payload)
    return response.json()

if __name__ == "__main__":
    email = "example@example.com"
    info = get_contact_info(email)
    print(info)
```

When we ran this, truth be told, Kenneth's jubilant clapping startled me. But it was real — the JSON blob we received (our ultimate prize that day) proved our communion with FullContact was sound.

### Scaling Up: Engineering for Growth

Now that we had a working interaction, the challenge was to make it scale like a cat climbing a tree — gracefully, and without getting stuck midway. Kenneth insisted we needed to shift to an architecture that allowed our application to evolve and grow, much like his hair, which seemed immune to taming.

#### Implementing Asynchronous Requests

One part magic, one part logic bending — async programming was the way forward. We needed to make sure our application could handle multiple requests without demanding the patience of a saint.

We strategically placed `asyncio` into our toolkit. With a slight tinker of `app.py`, we refracted our light into a more efficient spectrum:

```python
import os
import requests
import asyncio
import aiohttp

API_KEY = os.getenv('FULLCONTACT_API_KEY')

async def fetch_contact_info(email):
    url = "https://api.fullcontact.com/v3/person.enrich"
    headers = {
        'Authorization': f'Bearer {API_KEY}',
        'Content-Type': 'application/json'
    }
    payload = {"email": email}

    async with aiohttp.ClientSession() as session:
        async with session.post(url, headers=headers, json=payload) as response:
            return await response.json()

async def main(emails):
    tasks = [fetch_contact_info(email) for email in emails]
    return await asyncio.gather(*tasks)

if __name__ == "__main__":
    email_list = ["example1@example.com", "example2@example.com"]
    results = asyncio.run(main(email_list))
    print(results)
```

Now we could request information for multiple people at once, like a veritable communication symphony. This refinement was met with triumphant cheers — by both myself and Kenneth, who had finally found his tune.

### Final Thoughts: Reflecting on the Build

As we stepped back and surveyed our creation, it was akin to watching the first blooms of spring break through the earth — an acknowledgment of effort and resilience. A simple concept executed with grace, except without the threat of frost or bugs.

This development journey with FullContact was not just about parsing data but rather about learning and adapting — like Kenneth realizing finally, after multiple failures, the futility of attempting to harmonize with his parrot. We built something formidable and scalable, gaining insights that would certainly rescue us in future endeavors.

Let’s embrace the magic that is collaboration, be it with an API or a colleague who has questionable musical tastes, and explore the boundaries of our capabilities. Cheers to our collective journey in scaling up digital mountains with the FullContact API!