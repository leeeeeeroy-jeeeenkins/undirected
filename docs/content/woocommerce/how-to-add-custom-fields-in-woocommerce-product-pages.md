---
slug: how-to-add-custom-fields-in-woocommerce-product-pages
title: How to Add Custom Fields in WooCommerce Product Pages
authors: [undirected]
---


# How to Add Custom Fields in WooCommerce Product Pages

Ah, here we go, back to the days when Janet and I were sitting in her dimly lit attic, the place where inspiration either thrived or trembled from the weight of cobwebs. Janet, bless her heart, had this spark of genius mixed with the chaos of a toddler on a sugar rush. She passionately spoke about her online store of handcrafted marzipan marvels—and how every piece sold needed a heartfelt backstory, not just the standard weight and price labels that WooCommerce insisted on.

So, we embarked on this delightful journey to embellish her digital shelves with tales of almond origins and whimsical flavor inspirations. It seemed like a computer waltz—where code met imagination. And oh darling, it was the beginning of our adventure in adding custom fields to WooCommerce product pages!

## The Dance Begins: Understanding Custom Fields

Understanding custom fields—stay with me, folks, this is the gentle caress before the tango. WooCommerce is pretty much like a well-stocked pantry, practical but not personal. If you want to add flair (or a drizzle of passionfruit glaze, as Janet would say), custom fields are your go-to ingredients. They let you personalize product pages with extra info that resonates with your brand’s unique voice.

But why stop at features? Why not dive deep into the puddles of our limitless creativity and bath in these glorious customization fields?

## Setting the Stage: Meet the Players

Before we twirl into technical steps, let’s talk tools. Don’t worry; we're not carting wheelbarrows of jargon here, just the essentials. We're working in WooCommerce—our cozy e-commerce corner—nested within the grand WordPress mansion. We shall need a child theme and a shiny plugin called ‘Advanced Custom Fields (ACF)’. Remember, it’s just us, Janet, and a couple of cups of coffee.

### Getting Started with Advanced Custom Fields

First things first, you download and install the Advanced Custom Fields plugin. Sipping our coffees, we watched the progress bar, sharing a dance of anticipation. Once it was installed, it felt like the moment a magician reveals his deck—ready for tricks!

Head over to **Custom Fields -> Add New** in the WordPress dashboard. We called ours ‘Product Stories’, inspired by Janet’s most whimsical marzipan tale.

### Creating Your First Custom Field Group

Our next move was to create fields that tell a story. Click on **Add Field** and the magic unfolded:

- **Field Label** and **Field Type**: Here, our hearts sang. Label it something poetic like "Origin Story" and choose a type—text, image, or maybe a lovely WYSIWYG editor for creativity to flow.

- **Field Instructions**: This is where Janet could whisper sweet nothings—prompting each marzipan’s tale to unfold.

- **Location Rules**: We selected ‘Product’ because that’s where our marzipan odysseys want to reside—you select whatever matches your vision.

Remember, the fields you create are the brushstrokes on your WooCommerce canvas.

## The Code Waltz: Bringing Custom Fields to Product Pages

As the narrative of our mission unfolded, we rushed to our text editors, our fingers dancing an evolved tap dance of modern-day artistry.

### Step 1: Create a Child Theme

Ah, the child theme. Think of it as your playground where all creative experimentation happens without fear of losing existing charm. In your WordPress directory, create a folder named `your-theme-child`, and inside it, create a `style.css` and `functions.php`.

The `style.css` needs a header. Allow me:

```css
/*
 Theme Name:   Your Theme Child
 Template:     your-theme
*/
```

And in `functions.php`, enqueue the parent theme stylesheet:

```php
<?php
function my_theme_enqueue_styles() {
    $parent_style = 'parent-style';
    wp_enqueue_style($parent_style, get_template_directory_uri() . '/style.css');
    wp_enqueue_style('child-style', get_stylesheet_uri(), array($parent_style));
}
add_action('wp_enqueue_scripts', 'my_theme_enqueue_styles');
```

### Step 2: Display Custom Fields on the Product Page

In our journey, this was Janet’s ‘voila’ moment—merely lines of PHP, but they shimmered with potential. We edited the `single-product.php` in our child theme directory. Add this beauty wherever you want your custom field to appear:

```php
<?php
if (function_exists('get_field')) {
    $origin_story = get_field('origin_story');
    if ($origin_story) {
        echo '<div class="product-origin">' . esc_html($origin_story) . '</div>';
    }
}
?>
```

This is where your story lives. Right among the breadcrumbs of commerce, right there with the buyer’s gaze.

## A Sprinkle of Style: Custom CSS

Our souls were lifted by simple elegance. We added personal styling in the child theme’s `style.css`:

```css
.product-origin {
    background-color: #f1f1f1;
    padding: 15px;
    font-style: italic;
}
```

This was me adding a sprinkling of virtual saffron to an otherwise mundane plate. Suddenly, Janet’s marzipans were basking in a halo of chic.

## Graceful Encore: Testing and Tweaking

Of course, nothing ever goes exactly as planned on the first try. Ah, but there lay the beauty! We giggled at misplaced pixels, touched up with elegance born from absurdity, until each field sang a precise melody. You remember testing all this with a pretend customer’s eyes, don’t you?

Every product felt like a handcrafted serenade—a testament to hours spent with Janet, laughing over mugs of cooling coffee, lost in the code that bridged her world and her customers.

## Easing into Completion: Ready for the World

With the custom fields displaying beautifully or so we thought, we leaned back and marveled at our handiwork on the screen. It was more than code—it was Janet’s mastercrafted story living on a digital stage.

This journey—our shared adventure—reminded me of simple joys: the thrill of discovery, and the triumphant whisper of creation past midnight. Custom fields in WooCommerce became not just additions, but the vibrant strokes of our shared canvas.

Janet’s store was now an embodiment of her quirky self, each product page a personal letter to her customers. And, dear reader, as you venture into adding your own custom fields, remember this: it isn’t just a technical task—it’s art, collaboration, and a sprinkle of magic coding dust.

Here’s to every field telling a story—may your product pages reflect your spirit, and remember every bit is a part of your delightful WooCommerce symphony.