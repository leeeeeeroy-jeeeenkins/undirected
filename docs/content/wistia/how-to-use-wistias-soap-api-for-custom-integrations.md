---
slug: how-to-use-wistias-soap-api-for-custom-integrations
title: How To Use Wistias SOAP API For Custom Integrations
authors: [undirected]
---


# How To Use Wistia’s SOAP API For Custom Integrations

It was a crisp autumn evening, and the last rays of sunset painted my office walls a warm shade of orange. There I was, surrounded by an array of monitors displaying endless lines of code, coffee mug perched precariously on the edge of my desk. A notification popped up on my screen - "Wistia's SOAP API." Oh yes, that cryptic three-letter acronym was about to become my new best friend.

My friend Jake had called earlier that day. “How do we make the videos on our site talk to our CRM, Anna? Is that even a thing?” he asked, while juggling a conversation about his puppy’s ever-so-adventurous escapades with a neighbor’s garden gnome. An idea sparked. Wistia’s SOAP API might just do the trick for integrating custom tools, I thought, with Jake's puppy’s bark still echoing in my ear.

## The Dawn of Discovery: Setting the Stage

Our first step is straightforward and almost ceremonious - we needed to get the lay of the land. The vast terrain of Wistia's API documentation awaited us, brimming with promise and potential for discovery.

**First Stop: Documentation Land**  
Yes, I know - reading documentation is often like trying to assemble flat-pack furniture without the illustration. But fear not. Wistia's documentation, with its neat sections and straightforward language, was refreshingly clear. 

We discovered that before we could juggle video integrations, we needed a SOAP client. This was the magic wand, the wizard's staff, the humble tool we’d use to send our invocations to the Wistia video gods.

- **Step 1**: Get a SOAP client. Whether you prefer PHP, Python, Java, or any other language with a SOAP library, grab your weapon of choice. Personally, I went with Python’s `zeep`, because why not enjoy the benefits of an excellent parsing library with a quirky name?

```python
# Install zeep using pip if you haven't already
pip install zeep
```

## Our SOAP Star Begins to Shine: Authentication

Now, here comes the moment of truth - Authentication. Like asking a bouncer to let us into an exclusive club; without the suitable credentials, no entry for us. We needed to create an API token in Wistia.

**Easy-peasy, lemon-squeezy: Why, yes!**  
Head over to the Wistia dashboard, navigate to the Account Settings, and summon forth the “API Access” section. Here lay our sacred text - the API token.

- **Step 2**: Generate the API token.

```python
# Fetch API token from your Wistia account
api_token = 'YOUR_API_TOKEN'
```

With the token in hand, we commanded our SOAP client to include this in the header of every SOAP request we made. To seal the deal, we concocted a simple authentication script.

```python
from zeep import Client
from zeep.transports import Transport
from requests.auth import HTTPBasicAuth
import requests

# Your Wistia soap URL and Token
wsdl_url = 'https://api.wistia.com/v1/soap_wistia_api.wsdl' 
auth = HTTPBasicAuth(api_token, 'X') # 'X' as password placeholder

# Transport with authentication
transport = Transport(session=requests.Session())
transport.session.auth = auth

client = Client(wsdl=wsdl_url, transport=transport)
```

In Jake's words, "If you can't speak the language, you won't get anywhere in this land." And catapulted we were, into a world where video metadata dwelt, begging to be explored and manipulated.

## The Integration Juggernaut: Fetching Data

With our armor ready, it was time to start pulling data. We faced our first quarry: fetching a list of projects.

- **Step 3**: Let's retrieve all those projects.

```python
# Fetch list of projects
projects = client.service.list_projects()
for project in projects:
    print(project.name)
```

It was like opening a treasure chest! A cascade of project titles gleamed on our terminal screen. This, my friends, is what triumph looks like—a verbose, scrolling list of projects from Wistia.

## Wielding the Power: Manipulating Our Data

Once we were adept at calling forth the project names, we yearned for more. Could we upload videos? Fetch stats? Are we unstoppable?

### Uploading a Video
```python
# Upload a video to specific project
with open('path_to_your_video_file', 'rb') as video_file:
    client.service.upload(video_file.read(), project_id='PROJECT_ID')
```

As that video uploaded, I could almost see Jake’s puppy’s tail wagging in approval of our digital triumph.

### Fetching Stats
```python
# Get video stats
video_id = 'YOUR_VIDEO_ID'
stats = client.service.video_stats(video_id)
print("Plays:", stats.plays)
```

Fetching stats had us face-to-face with the aftermath of our integration work. Usage data, plays, all those analytics every marketer dreams about when they talk in weird spreadsheets at conference tables.

## Onward with Integrations: Final Thoughts

We had pulled off the unthinkable, tamed the SOAP API, and presented our findings with little fanfare - a sense of satisfied achievement hanging in the air as we powered down our machines.

The world of video and data stretched infinitely in front of us, waiting for creativity and innovation to become our guides. Jake’s puppy, forever the source of chaos and inspiration, played on blissfully unaware of the puppet strings pulled across this digital landscape to make our encounters ever more seamless.

In the end, integrating Wistia’s API into our system felt less like a technical hurdle and more like carving a path in a forest untamed. Quite enriching. We took on the challenge, learned new tricks, and had just enough fun to keep coming back for more. Through Wistia’s SOAP API, there were no secrets - we wrote our story, call by call, request by request, video by video.

And as we stood on the brink of another sunset, somewhere… Jake’s puppy was undoubtedly preparing his next adventure among garden gnomes. 