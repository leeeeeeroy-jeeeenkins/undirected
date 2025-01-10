---
slug: measuring-roi-of-your-customer-success-efforts-with-totango
title: Measuring ROI of Your Customer Success Efforts with Totango
authors: [undirected]
---


# Measuring ROI of Your Customer Success Efforts with Totango

I remember vividly the sun spilling through the office blinds on a Thursday morning. The coffee machine was belching its usual soundtrack while Sarah and I hunkered down at the conference table, armed with laptops and a little more optimism than usual. We had just launched some of our most ambitious customer success initiatives yet, and like anxious parents at a piano recital, we were eager to see if our efforts would hit the right notes. Would Totango shine a light on our successes, or would it expose us for the overly enthusiastic novices we feared we might be?

As Sarah plunked down beside me, muttering something about data points and dark magic, I realized that understanding the ROI of customer success efforts went beyond just spreadsheets and analytics. It was a quest for clarity in the tangled jungle of customer relationships. Armed with Totango—a tool promising us that very clarity—we embarked on a journey that would surprise us. So, pull up a chair as we dive into this delightful chaos of measuring ROI with Totango. It's more riveting than a Netflix series, I promise.

## Step 1: Define What Success Looks Like

Picture this: The scent of freshly baked cookies wafting through our pantry-sized meeting room. For us, defining success was like choosing between those warm, gooey cookies and a celery stick – it might be an obvious choice, but it still needed deliberation. Before we could start our measurement theatrics with Totango, we needed to pin down precisely what outcomes we were chasing: increased retention? Customer lifetime value uplift? More people high-fiving in our hallway? 

In Totango, this meant setting up campaigns and segments that resonate with our definition of success. “What do we want to achieve?” Sarah scribbled on a whiteboard, plus ten doodles. 

### Pro Tip

It’s critical to customize your metrics and KPIs in Totango to reflect goals that are as personal as a diary entry. Our terms of success differ; so, tailor them like a well-fitted jacket.

## Step 2: Navigating Totango’s Dashboard (Without a Helmet)

With our success criteria sprawled out like an architect’s blueprint, we turned our attention to the dashboard. If Totango were a theme park, the dashboard would be its roller coaster—full of highs, lows, and enough data twists to thrill (or terrify) our analytical senses.

To get a real ROI handle, you can sift through key metrics like Customer Health, Adoption Rates, and Renewal Likelihood. Perfume the extraction with the essence of curiosity. Sarah pulled open a metric widget and gasped, “Look! It’s like graphical art.” 

Don't skip the detail. Totango makes the metrics dance—watch carefully. Toggle between customer segments to visualize how different strategies impact different folks (or customer types, if we insist on being serious).

### Code Corner

Here's a simple code snippet to pull customer health scores using the Totango API for those who love to dig deeper:

```python
import requests

def get_customer_health(api_token, account_id):
    headers = {
        'Authorization': f'Bearer {api_token}',
    }
    response = requests.get(f'https://api.totango.com/api/accounts/{account_id}/health', headers=headers)
    return response.json()

api_token = 'YOUR_API_TOKEN'
account_id = 'CUSTOMER_ACCOUNT_ID'
print(get_customer_health(api_token, account_id))
```

Sarah giggled at the lines of code like she’d just read a Shakespearean sonnet. Poetry in digital motion.

## Step 3: The Science (or Sorcery) of Segmentation

Our office, with its quirky mix of decaf aficionados and caffeine zealots, was akin to our diverse customer base. Segmenting is where Totango truly flexed its muscles. A firm believer in the power of organization, Sarah likened it to a well-labeled spice rack: everything neat, categorized, and ready for action.

Segment your customers based on criteria that matter—industry type, engagement level, or maybe whether they appreciate our fabulous newsletter. The more intentional you are, the clearer your ROI picture becomes. 

### Anecdote Alert

Did I ever tell you about the time we segmented users by their survey feedback, only to realize all negative comments came from a single geography? Sarah called it geographic enlightenment.

## Step 4: Optimize and Tweak

Once you've laid the groundwork with data and segments, let's channel our inner Michelangelos and start chiseling. Much like when Sarah used to tweak Grandma's pie recipe, in Totango, it's about optimizing those efforts over time. 

Adjust the campaigns—if engagement flops, pivot. We realized that our webinar strategy needed roles swapped. (Our CEO isn't quite the charismatic speaker we'd hoped.) Totango offers insights into what's not working; trust the data, even if it means having tough conversations over lunch.

## Step 5: Crunching Numbers and Celebrating Wins

As the dust settled and we eagerly awaited the results, a quiet shout of victory filled our frothy cappuccinos. Was this what achieving nirvana felt like in the business world? Totango reports offer detailed insights with calculated ROI metrics—a veritable holy grail for number-crunching fanatics. 

Remember Steve, from sales? He donned his statistics hat and, for a moment, was our hero. Total nerd glory right there as he connected customer success activities directly to revenue results. 

### A Pinch of Humor

What’s better than seeing a positive ROI? Watching Sarah dance across the conference room when the graphs showed a notable uptick.

## The Totango Toast 

Measuring the ROI of customer success aspirations with Totango taught us more than just the raw numbers—it gifted us stories, learnings, and the occasional belly laugh. Our Thursday mornings are forever changed, just like our perspective on customer success metrics. It may not have been a flawless journey, but embracing Totango alongside a spirited team yielded dividends equal parts emotional and financial. 

To our collective delight, the quest for measuring ROI wasn't the dry lesson we expected but an exhilarating narrative—lit with bizarre happenings and triumphant moments. We now share Thursday success tales over those inevitably devoured cookies and commend Totango for transforming chaos into clarity.

In the end, it's a tale about not just striving for success but understanding it—one dashboard view and heartfelt anecdote at a time. Cheers to that! 🥂