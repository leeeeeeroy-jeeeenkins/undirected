---
slug: how-to-build-a-custom-theme-in-drupal-a-complete-guide
title: How to Build a Custom Theme in Drupal A Complete Guide
authors: [undirected]
---


# How to Build a Custom Theme in Drupal: A Complete Guide

## A Walk Down Memory Lane

Do you remember that feeling, when dipping your toes into the icy waters of a new skill? Let me take you back. There I was, perched on a squeaky chair in my cluttered living room, laptop precariously balanced among coffee mugs and a nest of cables. It was a Saturday morning, Seattle's drizzle pattering softly against the window. My curiosity had tugged me into the labyrinth of Drupal, where I, armed with naivety and enthusiasm, was determined to craft a custom theme. I wanted something unique and bespoke – none of those cookie-cutter designs would do.

Drupal. It had this mystique, like a secret club you could only join if you knew the secret handshake. I was intrigued. My first encounter was peculiar but exhilarating; I felt akin to discovering a hidden chamber in an ancient temple. Sure, the path was littered with bugs and typos, but importantly, it was mine. I'm here to share that journey with you, as we unravel the mystery of building a custom theme in Drupal – together. So grab a coffee (or tea if that's your flavor) and let's dive right in.

## Getting Started: Laying the Foundation

First off, like any good story or garden, it all begins with planting the seeds. But, remember, every gardener needs their tools. For this, you shall need Drupal installed on your local machine. If you haven’t done so, you might as well have started building a house without a foundation!

Installing Drupal might seem daunting, it’s like standing before a blank canvas with a multitude of paints. But, fret not, for it is far simpler than it seems. You can download it from [Drupal.org](https://www.drupal.org/project/drupal). Use a handy tool like Composer - think of it as your trusted steed - to gallop through this installation with ease.

```bash
composer create-project drupal/recommended-project my_site_name_dir
```

Setting up your local environment is akin to setting the mood for a grand performance. You want it just right. Platforms like XAMPP, WAMP, or MAMP provide local server support. Once installed, navigate to your new Drupal directory in your browser (typically something like `localhost/my_site_name_dir/web`). Set it up, create an account – and voilà, you're in.

### Crafting the Structure

Now, envision your theme as a bespoke suit, meticulously cut and tailored. In Drupal, themes live in the `/themes` folder. Let's create a directory for ours. Navigate to `web/themes/custom` and within this folder, make a new directory, something catchy like `awesome_theme`.

Next, we sketch the blueprint. We need to stir up a `.info.yml` file; consider it the birth certificate of your theme. In your `awesome_theme` directory, create `awesome_theme.info.yml`. Inside, let's define some details:

```yaml
name: 'Awesome Theme'
type: theme
description: 'A bold and striking custom theme.'
package: Custom
core_version_requirement: ^8 || ^9
```

If you hear a distant chorus of angels singing, it's just your theme coming alive.

### Our First Install

Hold my cup, it's time for the grand reveal. Head into the Drupal admin area (logins are lifesavers here) and navigate to Appearance, where you should see "Awesome Theme" gracing the list. Hit that suave "install and set as default" button. Ta-da!

## The Art of Styling

If designing the layout is building the walls, styling is adding that splash of color. Create a `css` directory inside `awesome_theme` and within, a `style.css` file. The magic of CSS comes alive here. You could style the body in the `style.css`, like this:

```css
body {
  background-color: #eaeaea;
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
}
```

In our `.info.yml`, let’s tell Drupal about this new styling magic:

```yaml
libraries:
  - awesome_theme/global-styling
```

And in your theme's directory, create `awesome_theme.libraries.yml`:

```yaml
global-styling:
  css:
    theme:
      css/style.css: {}
```

Reload your site. Bask in the resplendent joy that your stylesheet is working.

## Twig: The Designer’s Toolkit

When I first encountered Twig, it was like discovering an unexpected ingredient that made the recipe sing. Twig is our templating engine, our chisel and marble.

Twig files or templates govern the structure of your content. They reside in the `templates` directory. Picture this: you want to change how a page node displays. Go ahead, create `node--page.html.twig` inside `templates`.

```html
<div class="page-node">
  <h1>{{ node.label }}</h1>
  <div class="content">
    {{ content.body }}
  </div>
</div>
```

Now refresh, and you’ll see Drupal’s face subtly transformed by your code. It's akin to giving a statue a fresh expression - subtlety at its finest.

## Making It Interactive

JavaScript is like adding secret doors with hidden functions in a fantasy RPG. Imagine adding interactive flair. 

Create a `js` directory and a `script.js` file. Add a simple script:

```javascript
document.addEventListener("DOMContentLoaded", function() {
  console.log("The adventure begins!");
});
```

Update `awesome_theme.libraries.yml`:

```yaml
global-scripting:
  js:
    js/script.js: {}
```

Add the library to your theme in `awesome_theme.info.yml`:

```yaml
libraries:
  - awesome_theme/global-styling
  - awesome_theme/global-scripting
```

Check your console, relish the console.log as a victory cry. It's working!

## Beyond Basics: Hook Alterations and Preprocess Functions

Alright, now we’re venturing into deeper waters. Everything you see, parts of it can be altered using hooks and preprocess functions - your backstage magic.

Create a `theme-settings.php` in your theme's root. Use `hook_preprocess_HOOK`, where HOOK can be any base template name. Have you too felt the electrifying power of altering behavior without tedious overrides?

For instance:

```php
function awesome_theme_preprocess_node(array &$variables) {
  if ($variables['node']->getType() === 'article') {
    $variables['content']['#attributes']['class'][] = 'special-article';
  }
}
```

This subtly adds a class to article nodes; nothing too dramatic but oh so empowering!

## Conclusion: Watch as it Flourishes

What a journey! From the unassuming inception of a custom theme to watching it blossom with functionalities, it’s a labor of love. Like watching an acorn grow into a mighty oak tree – slow and steady, each step a testament to our work.

It was a little over a year since that Saturday dive when I built my first theme. Sitting here now, running my fingers across these keys, I hope our paths meet here with your burgeoning Drupal theme flourishing in your bustling to-do list, perhaps reaching new heights I never dreamed of on that rainy Seattle morning. Here's to your Drupal journey. An epic saga that intertwines your ideas with the endless possibilities of code and creativity. Cheers to creating something uniquely yours.