---
slug: how-to-connect-different-data-sources-in-qlikview
title: How to Connect Different Data Sources in QlikView
authors: [undirected]
---


# How to Connect Different Data Sources in QlikView

---

## A Cozy Beginning by the Flickering Glow of Our Monitors

It was a Tuesday evening with hazy golden tones filtering through my home office window, spilling like warm honey on the keyboard. Amy, my colleague and partner-in-all-crime at our small consulting firm, was a breath away behind her screen, daring her printer to misbehave. Our coffee cups sat cooling, forgotten. That's when we realized—a revelation as delightful as fresh popcorn during a plot twist—that connecting different data sources in QlikView could be, in its own way, like creating a symphony of diverse instruments.

We had spent the morning whipping up a data visualization for a client with more databases than shoes. The cluttered chaos begged to be transformed into a coherent narrative. This was not our first rodeo, and yet, the thrill of a new configuration, a new possibility, was palpable.

And so, off we trotted into the technical wilds of QlikView with the enthusiasm of hikers who just found a path less traveled.

## The Composition of Chaos: Setting Up Your QlikView Project

First things first, let's not dive headfirst into the deep end without our floaties. Before we even fire up QlikView, we need a game plan. Think of it as organizing a karaoke night—gather your tunes, know your singers. Align your data sources like the sensible adults we occasionally strive to be.

1. **Open QlikView**: No thrilling plot here—launch that sucker like the launch button of an intergalactic spaceship, sans the destruction potential.

2. **Create a New Document**: Click "File" and “New.” It’s as satisfying as opening a crisp notebook. 

3. **Access the Script Editor**: Now, this is where the magic happens. Hit "Edit Script..."—the ellipsis that holds a universe of possibilities—cue up the Script Editor. It’s your command center, folks.

## Poetry in Connection: Crafting Connections in QlikView

As we sat, ensconced in the glow from our screens, Amy mentioned that linking data in QlikView felt like matchmaking at its finest. Each table, a dashing singleton, waiting to be paired.

### Step 1: Declare Your Source Types

You’ve got choices galore—SQL Server, Excel, text files, you name it. QlikView doesn’t discriminate. If your data type is supported, it welcomes all types to the party.

- In the Script Editor, head to the “Database” tab for SQL sources or “Table Files” for others. Select your weapon of choice. Let’s assume a tangible example—an Excel file in our case, easy to grapple with.
  
```plaintext
LOAD FName, LName FROM
ExcelFile.xlsx
```
The basics are, well, basic, but don’t let their simplicity fool you—these are the sprightly steps to greatness.

### Step 2: Connecting to Multiple Sources

You might ask, "How does our Excel file mingle with that SQL database table without it turning into a perplexing love triangle?" Fret not, the answer is delightful:

- Hit up "Select Data" and choose "ODBC" or "OLE DB" to set up a SQL connection. Here, it’s all in the driver's details—choose wisely as you waltz through the connection wizard. Like a fairy godmother, it equips you with credentials and lets you save that beautiful string of connection goodness.

```plaintext
ODBC CONNECT TO [YourDatabase] (XUserID is ABC, XPassword is 123);
```
See? Now CREATE harmony by loading data across multiple sources with elegant conflict-resolution skills.

## Harmonizing the Melodies: JOIN-ing Tables

In the heart of our adventure, we knew that visual storytelling requires seamless symphony. Welcome to the dynamic duet of your data sources.

### Step 3: Writing the Load Script

Inhaling deeply, like that moment before the first note of a concert, we wrote our script. Amy loved this part—the poet within her relished weaving data entities into a coherent tapestry.

- In your Script Editor, load and join tables. A simple `INNER JOIN` or `LEFT JOIN` can make all the difference.

```plaintext
INNER JOIN (ExcelFile) LOAD
EmployeeID, Salary
SQL SELECT EmployeeID, Salary FROM EmployeeSalaries;
```
Despite their directness, these commands cast complex shadows, conjuring cohesive data amalgamations.

### Step 4: Check the Synthesis

Review the data model like a painter scrutinizing their canvas. The Table Viewer becomes your magnifying glass—press Ctrl+T, see the web of your masterpiece. Tables intertwine, blossoming into something greater.

In the stillness, Amy remarked how akin this was to brewing the perfect coffee—distinct flavors merging into a beautiful whole.

## Striking an Encore: Refreshing & Troubleshooting

Amy shifted in her chair as we pondered the importance of keeping the connections alive and kicking. 

### Step 5: Refresh Your Data

Data’s a living creature—it changes, grows, and sometimes unexpectedly mutates. We refresh using neat scripting magic or the good old-fashioned manual update.

- Set up automatic reload tasks in QlikView Server if you’re posh and have access, or teach your users to hit the “Refresh” button with gusto whenever needed.

### Step 6: When Things Go Sideways

The journey, like yours or ours, is sprinkled with rogue tripwires. Embrace problems as opportunities to flex your troubleshooting might. Common headaches include connection issues or uncooperative data types.

- Check error logs in QlikView or assert keyword detectives to analyze the discrepancy.

```plaintext
LOAD *,
  IF(IsNull(Name), 'Unknown') AS Name_Fallback
RESIDENT YourTable;
```
Keep experimenting, tweaking, and embracing the glitches with such zest that bugs beg for mercy.

## A Joyous Conclusion

At the end of our sonorous escapade, Amy and I sat back, hit save, and cheered our screens with mugs of lukewarm coffee. Our datasets sang in chorus, robust and mellifluous. Simple scripts, profound connections, and a hearty dash of persistence—there’s our QlikView tale.

As our journey attests, connecting different data sources in QlikView isn't just a technical task. It’s a dance—a collaboration between you, your tools, and the stories your data longs to tell. Let’s lift our sleeves together, embrace the chaotic harmony, and celebrate these shared moments of data connectivity.