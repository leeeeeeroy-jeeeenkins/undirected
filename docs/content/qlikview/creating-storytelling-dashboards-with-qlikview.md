---
slug: creating-storytelling-dashboards-with-qlikview
title: Creating Storytelling Dashboards with QlikView
authors: [undirected]
---


# Creating Storytelling Dashboards with QlikView

Once upon a time, perhaps longer ago than my memory cares to admit, our team faced a peculiar challenge — we had data, lots of it, but it was soul-crushingly dull. Numbers and charts that could make a night owl fall asleep before dusk. It was like staring at a digital wasteland of columns and rows, devoid of any semblance of narrative or intrigue. Then, during an innocent coffee break — a moment that seemed ordinary but turned extraordinary — Liliana, our vivacious data analyst with a penchant for the dramatic, recounted how she imagined each subset of our dataset as a character in a grand narrative. It was a revelation. Why couldn't our dashboards tell stories too?

This idea flickered in our minds like a candle struggling against the wind. We needed a tool to breathe life into our static tableau, something imaginative yet feasible. And so, our odyssey with QlikView began.

## The First Spark: Falling in Love with QlikView

Our first encounter with QlikView was a bit like meeting a celebrity crush for the first time — excitement mingled with the very real possibility of disappointment. Introduced by Eduardo, our maverick IT guy who always seemed to be one step ahead of digital trends, QlikView promised us a new lease on data life.

The revelation struck me as we huddled around Eduardo's laptop, sipping on hastily prepared espressos. With a few deft clicks, he spun data into a whirlwind masterpiece — dashboards that narrated stories; they spoke, questioned, and enlightened. Suddenly, data points became protagonists, and metrics turned into plot twists. We found ourselves gasping at the vibrant palettes and intuitive designs. This was more than love; it was destiny.

### Getting Hands-On: Building Our Narrative Framework

Setting up QlikView was, surprisingly, a bit like assembling flat-pack furniture: ostensibly straightforward but unexpectedly nuanced. A nose dive into the how-to wasn't intimidating; it felt like an opportunity to craft our first 'novel' in dashboard form.

1. **Install and Setup**: We started simply. Downloading and installing QlikView from [Qlik's website](https://www.qlik.com). It was as swift as Eduardo promised — no plot twists here.

2. **Data Loading**: Feeding data into QlikView was akin to casting the characters in a play. We utilized the ‘Script Editor’ section, a powerful beast that required taming. Connecting to our various data sources - a flurry of SQL databases and Excel sheets - felt like arranging a chaotic prose into poetic harmony.

    ```sql
    LOAD 
      CustomerID, 
      EmployeeID, 
      OrderDate, 
      ShipCity 
    FROM 
    [..\Data\Orders.xlsx]
    (ooxml, embedded labels, table is Orders);
    ```

3. **Crafting Sheets**: Each sheet was a chapter in our grand novel. Visualization widgets (graphs, tables, and buttons) were our words, and we sprinkled them with enthusiasm across our digital canvas. Eduardo had a knack for colors, and his artistic vision made each sheet pop like a comic book panel.

4. **Storytelling Elements**: Diving deeper, we discovered Qlik’s ‘Storytelling’ feature. It let us stitch together narratives that would rival any paperback thriller. We dragged and dropped key data insights, adding captions to weave a coherent tale.

5. **Interactivity**: Vital to our storytelling were the interactive elements. These were the plot twists — filters and drill-down options that engaged users, inviting them to explore stories within stories by merely clicking through visuals.

    ````
    SET vYear = Year(Today());
    ````

Liliana was ecstatic, and asked if it was possible to overlay a dramatic sound effect on interaction — alas, perhaps technology isn't ready for that degree of drama yet.

## A Journey of Visuals: Embracing Artistry in Data

QlikView turned us from mere analysts into digital artists. Michaela from accounting — an unexpected data virtuoso — likened designing dashboards to painting urban landscapes, chaotic yet fundamentally structured. Our dashboards, now far beyond rudimentary fact-sheets, were like canvases telling tales of fiscal triumphs and market shifts — sometimes with cliffhangers that demanded interpretation.

### Colors and Layouts: Our Digital Paintbrushes 

The design phase made us realize something; we're artists at heart, even if our brushes were charts and palettes entrenched in hexadecimal codes. Color schemes were crucial, as they were the emotional heartbeat of our dashboards. Contrasting hues were championed, bringing out trends and anomalies with dramatic flair.

Liliana insisted on adding a splash of yellow — she swore it sparked joy, and we couldn’t disagree. We even created a character named ‘Yello’, a jaunty yellow pie chart that became our unofficial mascot. We joked that he represented the happy slice of data — never failing to uplift team meetings.

````
ColorMix1(Avg(Sales), Blue(), Red())
````

## The Plot Thickens: Utilizing QlikView Functions

As we deepened our bond with QlikView, its functions became our trusted toolbox. They were the backbones of our data stories, providing context, conflict, and resolution.

### Thematic Analysis with Set Analysis

Set Analysis was our literary device, enabling us to examine 'what-if' scenarios across sprawling data landscapes. It let us pose questions and hypothesize outcomes. Eduardo often waxed poetic about the layering depths and dimensions it uncovered. 

````
Sum({$<Year={$(vYear)}>}[Sales Amount])
````

### Variables: Our Dynamic Plot Devices

Variables were another feat of storytelling magic. They allowed us to modify whole plots without rewriting the entire story. Much like a newspaper columnist might adjust an editorial stance based on unfolding events, we used variables to adjust narratives on the fly — without altering the overarching theme.

## The Climax: Our Dashboard Debut

The big reveal came on a Monday. Nerves and excitement wound through us like intertwined vines. Our collective effort, painstaking as it was rewarding, was finally ready for its debut. The dashboards splashed across our presentation screen like the opening night of a highly-anticipated play — we watched, breathlessly, as our audience interacted with each element. Each click was a resounding success, each insight a standing ovation.

Colleagues who had once dreaded quarterly data reports were now actively engaging, predicting outcomes, and making informed decisions — all while enjoying the 'performance'. Our dashboards were no longer numeric landscapes; they were stories that leaped, danced, and twirled with each presentation. What had started as a mundane exercise transformed into shared narratives that bridged gaps and brought people together.

## Reflection: The Joy of Storytelling

Reflecting on our journey with QlikView, we realize we've not just transformed how we use our data, but how we see ourselves — as part of a grander narrative where every byte and pixel has its place and importance.

The heat of those coffee-fueled brainstorming sessions, the sighs of Jessica’s frustration turned relief, the chuckles over ‘Yello’ and impromptu dance breaks to shake off the tedium — they were all stories within our story. In our hands, data became more than numbers; it became the language of collaboration, exploration, and discovery.

And though our story with QlikView is still unfolding, each dashboard, graphic, and insight becomes more than a tool — it becomes part of our collective tale, ours to tell and retell with every new chapter. We end our day hopeful, anticipating the twists and turns of our data stories, ready for what the next plot twist will bring.