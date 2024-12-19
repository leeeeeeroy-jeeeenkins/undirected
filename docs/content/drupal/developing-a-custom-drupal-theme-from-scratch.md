---
slug: developing-a-custom-drupal-theme-from-scratch
title: Developing a Custom Drupal Theme from Scratch
authors: [undirected]
---


# Developing a Custom Drupal Theme from Scratch

I recall one crisp autumn morning when my friend Clara and I sat huddled together at her favorite café, sipping scarves-worth of warm chai latte while brainstorming ideas for her blossoming art website. She looked at me, eyes twinkling with excitement, and posed a challenge. "Why don't we build a custom Drupal theme?" My heart raced at the thought, more out of trepidation than thrill. We had never ventured beyond ready-made themes before, but there was something electric—something wonderfully terrifying—about creating something entirely our own. Little did I know, this decision would lead us down a rabbit hole filled with discovery, occasional frustration, and ultimately, a profound sense of accomplishment.

## Setting the Stage: Installing Drupal

Remember when we just skated through the installation and were suddenly in? That's where our journey began. So, first things first, we needed a fresh Drupal installation. You know, the thrill of typing `drush site-install` gives a rush akin to starting a new novel. We paced through the setup: creating a database, ensuring all server requirements were in tune, and soon—voila!—our Drupal site stood before us, a blank canvas ready to be colored with creativity.

To install Drupal, download it from [Drupal.org](https://www.drupal.org). Unpack it into your web server's directory. Set up your database, then swing by your browser and load it up with `http://localhost/drupal`. Follow the instructions, sip coffee slowly, and breathe.

## Laying the Foundations: Setting Up a Base Theme

As we sat discussing colors and layouts over more chai, we realized the importance of a strong foundation—in themes as much as anything else. So, we decided to use a base theme. The choice fell upon Classy, with its elegance and structure, which reminded me of that one time we attempted to paint over a crooked wall without fixing it first—lesson learned.

To utilize Classy, head to the `themes` directory inside your Drupal root, and create a new folder for your custom theme. Suppose Clara's Art was our theme name, the folder name could be `claras_art`.

Now, every great theme needs a `.info.yml` file. Let's create `claras_art.info.yml`:

```yaml
name: 'Clara\'s Art'
type: theme
base theme: classy
description: 'A custom theme for Clara\'s art website.'
core: 8.x
libraries:
  - claras_art/global-styling
regions:
  header: 'Header'
  content: 'Content'
  footer: 'Footer'
```

Definitely just the beginning, but such a beginning brings a sense of "this is real".

## Styling the Canvas: Adding CSS and Libraries

Clara always said a painter’s job isn't merely painting but understanding the dance of light and shadow—something similar happens with CSS in theming. We wanted our website to reflect Clara’s vibrant personality, so custom styles were a must. 

We created a `libraries.yml` file in `claras_art` directory:

```yaml
global-styling:
  version: 1.x
  css:
    theme:
      css/styles.css: {}
```

Simply put, this file makes sure Drupal knows our CSS wants to be known. Like mailing invitations to our own style party.

Inside `css`—aha, the glorious stylings awaited—we added `styles.css` (don't forget this part, it’s crucial!):

```css
body {
  font-family: 'Arial', sans-serif;
  background-color: #f0f0f0;
}

.header {
  color: #333;
  margin: 0;
  padding: 1rem;
  background-color: #fff;
  text-align: center;
}
```

Basic, yet nurturing creativity. Clara loved how those simple lines made the page pop, and just like that day painting just one wall a vivid shade brought our room to life.

## Crafting Unique Layouts: Templating with Twig

The sun dipped lower as we reached this stage, and tables around us began clearing—but not our enthusiasm! Twig became our new best friend, more reliable than any paintbrush. With it, we sculpted the magic of Clara's vision into reality.

Templates live inside `templates`—aptly named, no less! We started by creating `page.html.twig` within:

```html
<!DOCTYPE html>
<html {{ html_attributes }}>
  <head>
    {{ head }}
    <link rel="stylesheet" href="{{ directory }}/css/styles.css">
  </head>
  <body {{ body_attributes }}>
    <header>
      <h1>Welcome to Clara's Art</h1>
    </header>
    <div class="main-container">
      {{ page.content }}
    </div>
    <footer>
      <p>&copy; {{ "now"|date("Y") }} Clara's Art</p>
    </footer>
  </body>
</html>
```

We structured this knowing our audience would be experiencing Clara's world in every stroke and line.

## Breathing Life: Adding Interactivity with JavaScript

Remembering a whimsical moment when Clara tossed a splash of water on her canvas—pure experimentation, the same spirit led us to JavaScript. Our theme needed interactive flair, gentle touches of the unexpected—because art thrives there.

Create a `js/script.js` within your directory:

```javascript
document.addEventListener('DOMContentLoaded', function() {
  document.querySelector('.header').addEventListener('click', function() {
    alert('Welcome to Clara\'s art gallery!');
  });
});
```

Meanwhile, don't forget to inform Drupal about your mighty script—treat `libraries.yml` to include this:

```yaml
global-styling:
  version: 1.x
  css:
    theme:
      css/styles.css: {}
  js:
    js/script.js: {}
```

Upon seeing this come alive on her site, Clara’s smile doubled in size. Our efforts mingled like colors blending seamlessly on a painter’s palette.

## Fine-tuning: Testing and Debugging

Facing finished errors—or art pieces, which side are you on?—we tweaked and tested everything. Clara stayed close, her insightful critiques were invaluable. We discovered a joy unique to fixing broken code—a task no less creative than art itself.

Ensure theme debugging is enabled in `sites/default/services.yml`:

```yaml
parameters:
  twig.config:
    debug: true
```

We checked, rechecked—no dropped commas, no misplaced colons shall ruin us today! Errors fixed, cleaner than ever, Clara thanked the little features tested with cheers equal to a high-risk gallery unveiling.

## Final Flourish: Deploying Your Creation

At last! Clara’s digital masterpiece stood tall and proud. With a final café clink of remaining chai cups, we moved to deploy. Whether you host it on Pantheon or Acquia, or directly on some intrepid server, ensure you use **Git**—the unsung hero of version control.

And again, just like that autumn morning when it all started, we stared at our work. A theme both uniquely Clara’s yet interwoven with traces of our journey together. Watching the website live, we beamed, hearts equally full; we had arrived, forever changed by the experience crafted from scratch.

In closing, our shared adventure shows that with grit, a dash of humor, and a second pair of eyes—the sky's the limit. Developing a custom Drupal theme from scratch isn't merely techie work; it's like painting memories with a forever-kind of brush. Keep hacking, keep painting, and remember to enjoy the view.