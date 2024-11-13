---
slug: how-to-set-up-your-first-course-in-docebo
title: How to Set Up Your First Course in Docebo
authors: [undirected]
---


# How to Set Up Your First Course in Docebo

I still remember the first time I clicked on the “Create New Course” button in Docebo. My fingers hovered above the keyboard as if they had sprung roots overnight, the way you do when you're certain the wrong click could end life as we know it or, more realistically, create a pair of distorted learning pathways. We've all been there—staring at a screen with a mixture of hope and terror, hand clutching a coffee mug blazoned with motivational quotes. But I was ready, fueled by caffeine and determination. Let's dive into that tale.

## The Dawn of Initialization

It took me back to when Aunt Beatrice taught me to ride a bike—her voice steady but with that undeniable twinge of excitement. “Don’t just look at the pedals, look ahead,” she’d said. It's like that with setting up Docebo: we need the basics dialed in to make sure future you, course expert extraordinare, isn't cursing present-day you. Let's open up Docebo and click on **Manage Courses**.

### Step 1: Creating the Container for Knowledge

Start by clicking that enticing **New Course** button. Think of this as planting seeds in a classroom garden—you’re not just inputting data; you're nurturing sprouting minds. Next, name your course. Make it something memorable, like “Introduction to Ninja Algebra,” or whatever suits your fancy academic flair. Enter a unique course code. Don’t overthink it: simple codes like "ALG101" are your friends here—for when you squint at your spreadsheet before your second quadruple espresso of the morning.

### Step 2: Craft Your Course Details

Aunt Beatrice would say, "A bike isn’t just about wheels; what's the story?" This brings us to the course description—a short text to channel your inner wordsmith. Delight in describing what makes this course special, how it transforms knowledge into poetry in motion. After all, engaging text is a precursor to an engaging online experience.

## Building the Course: Assemble the Pieces

Back at the family gathering, Uncle George would start his puzzle-solving stories with a dramatic flair, the kind you might apply to perpetually crooked puzzle pieces. Fast forward to our Docebo adventure, we now move to **Course Management** like the puzzle champs we are—or at least aspire to be.

### Step 3: Adding Training Materials

Ready for the pièce de résistance? Clicking **Training Materials** is like opening a window to information galore. You'll find several options such as video files, PDFs, presentations, and more. Just imagine you're curating a tiny library, a digital treasure trove.

Upload your first video file by dragging it from your loyal folder or clicking **Upload**. Pro tip: Sometimes folder gremlins sneakily rename files, so double-check that “Final_Video.mp4” is, indeed, final.

Here’s some code for uploading content, if you’re automagically techno-savvy:

```javascript
function uploadMaterial(fileName) {
  const filePath = `./materials/${fileName}`;
  // Assume we have a Docebo API method here
  Docebo.upload(filePath, function(success) {
    console.log(success ? "Upload successful!" : "Upload failed!");
  });
}
uploadMaterial("Final_Lesson.mp4");
```

### Step 4: Structuring Modules & Lessons

Don your architect’s hat because structuring your modules is akin to building a digital Hogwarts—but with less chance of enchanted mishaps (we hope). Click on **Course Player**, and then add modules and lessons, stacking them like carefully arranged books in the library of Alexandria—and definitely less flammable, thanks to technology.

Don’t shy away from playfulness in titling: "The Art of Tactical Staring" Lesson 1, isn’t just memorable; it breezes past those hesitant first clicks learners make.

## Setting Boundaries: Course Settings and Visibility

Do you remember Cousin Sue, always insisting on defining playtime rules before every Monopoly game—an underappreciated thinker? Inspired by her wisdom, let’s shape our online course’s rules of engagement.

### Step 5: Configuring Course Settings

Head to **Advanced Settings**. Here you'll cross swords with parameters on course evaluation, completion criteria, and even certificate rewards. Decide if your course is an elite invitation-only club, or a bustling public forum. Personally, I find making courses invisible to the wrong hordes—like email inbox clutter—is particularly liberating.

**Example settings code:**

```json
{
  "evaluationType": "Test",
  "completionThreshold": 80,
  "accessibility": "Public"
}
```

### Step 6: Setting Up Enrollment

Channel your inner Cousin Sue and venture into **Enrollment Settings**. Here you decide the flow—whether it's exclusive and invite-only, or a cacophony of excited learners beating down your virtual door.

Adjust user-registration settings and decide on defaults. If you're feeling grand and benevolent, open it up to autonomously enroll—our little digital kingdom burgeoning with eager minds.

## Launch: The Grand Reveal

Remember our first bike ensemble with Aunt Beatrice, as the tires wobbled over concrete? It was time to fly; shaky at first but zestful. We’re now at a moment like that, ready to launch.

### Step 7: Course Go-Live

Once all’s set and structured, initiate the final bow by clicking **Publish**. You're not just sending data into the void, but launching a facet of your teaching spirit into the universe. With a click, the course embarks. Share your creation—unleash it! Post a friendly GIF on your digital bulletin board, or perhaps a triumphant newsletter.

## Aftermath: Learning the Ride

Back in the day, retries were Casey’s friends during his paper-airplane phase. Likewise, once your course has been released, feedback and iteration are pépites of wisdom. Encourage feedback and observe learner analytics. Use this data to adjust, tweak, renew—and get ready to build again.

As we take a step back from this little voyage through Docebo setup, remember each curve, each giggle, each eureka moment is a shared adventure. Aunt Beatrice was right: don’t just look at the pedals; look ahead. As we continue to create and educate, let's carry forward that delightful, hesitant eagerness. And when you're ready, there are future courses waiting for creation, each one a new story yet to unfold.

Now that the coins jingled in the merry solitude of your completed course, brew another cup, have a cookie—because the thrill of teaching has only just begun.