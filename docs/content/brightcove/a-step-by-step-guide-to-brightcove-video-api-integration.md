---
slug: a-step-by-step-guide-to-brightcove-video-api-integration
title: A Step by Step Guide to Brightcove Video API Integration
authors: [undirected]
---


# A Step by Step Guide to Brightcove Video API Integration

## A Dance with Code and Playlists

The first time we attempted to integrate the Brightcove Video API, it felt a bit like trying to learn the tango. There we were, code in one hand, coffee in the other, moving awkwardly around the development floor. Our new client, Annie—well-known for her love of video libraries—had a vision: create a seamless, spectacular video experience on her platform. At first, the concept seemed daunting. Brightcove's documentation stared at us with the intensity of a dance instructor unimpressed by our two left feet. Somehow, though, step by step, code by code, we started moving to a rhythm.

### 1. Setting the Stage: Getting API Credentials

Before we can glide across the integration floor, we must first acquire our API credentials. Think of this as the moment we get our dance card approved. First, Annie set us up with access to Brightcove's back-end. Connecting to the [Brightcove Video Cloud](https://studio.brightcove.com/products/video-cloud) meant creating a new application through the Brightcove Developer Portal. Here's how we did it:

1. **Sign up or Log in to Brightcove**: Once we had our Brightcove account, we clicked on the "Developers" tab.
2. **Create a New Application**: Located within the "API Authentication" section, we chose to create a new application. This involved selecting the APIs we wanted access to (hint: we chose all, just to be safe).
3. **Take Note of Client ID and Secret**: Like any good partnership, trust was key. We secured our Client ID and Client Secret, tucking them away for safekeeping.

This initial setup felt satisfying—as if, for the first time, we knew which way was left and which way was right on this coding dance floor.

### 2. Warming Up with Authentication

Our next step was learning how to authenticate our requests, which felt a bit like finally getting our dance shoes tied snug. Brightcove requires OAuth 2.0 for secure API access, and here's how we tackled it:

1. **POST Request with cURL**:
   We found a workable snippet online (thank you, internet gods) to acquire an access token:

   ```bash
   curl --request POST \
   --url https://oauth.brightcove.com/v4/access_token \
   --header "Authorization: Basic [base64 of client_id:client_secret]" \
   --header "Content-Type: application/x-www-form-urlencoded" \
   --data "grant_type=client_credentials"
   ```

2. **Understanding Responses**: The response gave us our access token—our golden ticket. We learned that tokens expired after a period, much like our dance enthusiasm after too many runs.

We saved the access token to be reused in subsequent requests, ensuring our dance continued uninterrupted.

### 3. The Heart of the Dance: Fetching Videos

For Annie’s project, the real show was fetching video data. We needed the music—the resources to make her platform truly sing. This part of the process felt like finally hearing the first notes of our favorite tune.

1. **Listing Videos**:
   
   Making a GET request to retrieve a list of videos was straightforward:

   ```bash
   curl --request GET \
   --url https://cms.api.brightcove.com/v1/accounts/[account_id]/videos \
   --header "Authorization: Bearer [access_token]"
   ```

2. **Filtering and Sorting**:
   
   It was crucial to sort through videos and select only the best performers. We played around with `q` parameters and perfected our search queries like:

   ```bash
   --data-urlencode "q=tags:('featured')" \
   --data-urlencode "sort=created_at"
   ```

Brightcove's filtering options were surprisingly agile, letting us twirl through content with elegance and ease.

### 4. Promenade: Uploading Videos

Uploading videos might have seemed like a simple lift, but it required some choreography. we had to consider pre-upload steps, and Brightcove did not disappoint with its requirements. We tackled it bit by bit:

1. **Create Video Object**:
   
   We prepared the video object with a little JSON structure:

   ```json
   {
     "name": "Annie's First Show",
     "description": "An exclusive look",
     "tags": ["Exclusive", "FirstShow"]
   }
   ```
   
   This request to `/v1/accounts/[account_id]/videos` taught us patience—there was beauty in getting video metadata just right.

2. **Upload Video File**:

   Brightcove wanted an intermediary step like a polite bow. We obtained an upload URL, aligning our request right to ensure proper submission:

   ```bash
   curl --request POST \
   --url https://ingest.api.brightcove.com/v1/accounts/[account_id]/videos/[video_id]/ingest-requests \
   --header "Authorization: Bearer [access_token]" \
   --header "Content-Type: application/json" \
   --data '{
       "master": {
           "url": "[upload_post_url]"
       }
   }'
   ```

With breath held, we watched our video join the virtual stage.

### 5. The Finale: Player and Playback

Finally, we reached the culmination of our efforts—integrating video players for audience enjoyment. Imagine Annie’s excitement, as this part was her crescendo, the moment her audience eagerly awaited.

1. **Get Player Info**:
   
   Players could make or break the viewership experience. We honed in on playlist features, adding skins and settings with:

   ```bash
   curl --request GET \
   --url https://players.api.brightcove.com/v1/accounts/[account_id]/players/[player_id] \
   --header "Authorization: Bearer [access_token]"
   ```

2. **Personalize the Experience**:
   
   We bestowed the videos with hooks and charms, adding customized options—just like fitting our dance shoes with comfy insoles:

   ```json
   {
     "logo": {
       "image": "[logo_url]",
       "link": "https://www.anniesplatform.com"
     }
   }
   ```

The result? A platform that felt personal, playful, and perfectly poised for users.

## The Curtain Call

As we integrated the Brightcove Video API into Annie’s platform, the journey felt breathtaking. Each step was a testament to patience, learning, and laughter. We, who began as awkward shufflers, emerged as confident dancers ready to take on new challenges with heartfelt enthusiasm. Remember to breathe, and celebrate each little success—just like that first perfect step on the dance floor. Dance on, brave coders. Let's keep making magic together!

This storytelling approach accompanied every fiasco and win, reminding us that creativity and technology dance best side by side, hand in hand.