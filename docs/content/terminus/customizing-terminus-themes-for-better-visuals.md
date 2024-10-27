---
slug: customizing-terminus-themes-for-better-visuals
title: Customizing Terminus Themes for Better Visuals
authors: [undirected]
---


# Customizing Terminus Themes for Better Visuals  

It was a rainy Sunday afternoon, the kind where the sky feels more like a giant gray blanket than a beacon of sunlight. My cat, Stella, sat purring beside me as I absentmindedly scrolled through endless lists of themes and fonts, seeking the perfect visual delight for my terminal. Why? Because why settle for bland when there’s an entire cosmos of customization out there? The endless seas of sameness were getting under my skin, like an itch I couldn't scratch. Then it hit me—a eureka moment sparked by my own sheer boredom. Why not tailor the Terminus to match our unique inner world's idiosyncrasies and quirks? 

### Recognizing The Need for Personal Aesthetic

I remember when my friend Lucas, the tech wizard, scoffed at my default settings. "Default is for the faint of heart," he teased, nudging me into action. It's funny how a playful taunt can ignite a cascade of change. Terminus, with its robust, if somewhat utilitarian, default settings, beckoned us to venture into its visual possibilities. But first, one needs to accept, as I did, that bland is not the companion we choose for our digital adventures.

### Experimenting with Colors: The Palette Playground

We’ve all seen it—painfully bright colors that could pierce through even the strongest filters of visual apathy. Sitting hunched over our screens, we find ourselves asking—do we let these default schemes dictate our mood? Our fledgling journey into color customization starts with a gentle tug-of-war with the hex codes. Just simple little bytes of magic! Open the Config.json file and let's start painting! Here’s what we did:  

```json
"colorScheme": {
    "name": "Custom Scheme",
    "background": "#212121",
    "foreground": "#E0E0E0",
    "black": "#000000",
    "red": "#D32F2F",
    "green": "#388E3C",
    "yellow": "#FBC02D",
    "blue": "#1976D2",
    "magenta": "#7B1FA2",
    "cyan": "#0097A7",
    "white": "#FFFFFF"
}
```

Each hex code a brush stroke in our digital masterpiece. Stella the cat gazed on approvingly, wise in her feline understanding of aesthetics.

### The Font Affair: Typography Meets Terminal

Lucas, bless his adventurous soul, often claimed that choosing the right font was akin to finding the perfect coffee bean. You never understand its impact until you've lived it. Ah, the simple joy of watching code flow across your screen in a beautifully chosen typeface. We plunged into Terminus settings:   

1. Navigate to Preferences.
2. Select Profiles and find Text.
3. Click Change... next to Font.
4. Try out fonts like “Fira Code” or “Consolas,” we found them to be both elegant and functional.

Finding the right font is like listening to a soothing melody while sipping an exquisite brew. 

### Incorporating Visual Plugins: Adding Some Jazz

It was during this phase that my cousin Marie, who is often mistaken for an artist trapped in a coder's body, pointed her paint-stained fingers at VS Code's extensions. "There’s treasure here," she declared, and she was right. The real fun began with plugins like Oh My Zsh, to streamline our look with beautiful prompts. Here's the initial set up:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Then, we added themes and custom plugins to make the terminal sing like a nightingale with a secret.

### Painless Workflow: Setup Your Path to Zen

You know those days when everything aligns just perfectly, and your workflow feels like a well-conducted orchestra? Our terminal journey reached such a crescendo when we stopped resisting the built-in capabilities—alias commands which tucked away hideous, verbose command lines for good.

```bash
alias gs='git status'
alias ll='ls -lah'
```

Simple aliases: a millennia-old shortcut to enlightenment. Stella, our resident fluff, stretched contentedly, suggesting she approved of this meditative harmony.

### Final Touches: Personal Icons and Emojis

“Why don’t we sprinkle in a dash of humor?” Marie piped up again, eyes alight with impish glee. And so, small whimsical modifications like icons at prompt lines (Star Wars characters anyone?) or emojis—yes, emojis—nestled snugly in our terminal interfaces, took residence, sparking joy in unexpected places. Emoji prompts are a playful way to remind ourselves never to take life—or coding—too seriously. Here’s how they found a home:

```bash
# Example of zsh prompt with emoji
PROMPT='%F{cyan}%1~ $(git_prompt_info)%F{yellow}⚡%F{reset} '
RPROMPT='%F{green}%n%F{reset}'
```

### Reflecting On Our Journey

Lucas, Marie, and of course, Stella, stood witness to our metamorphosis. Our transformed terminal environments aren't just functional— they resonate with personality, reminding us that our tools should inspire, not merely suffice. We've learned, adapted, and most importantly, we've reflected a part of our identity onto our workspace. And just as that rainy afternoon turned into a sunlit horizon, so too did our once-dreary terminal become our visually comforting, creative haven.

It's been a journey of discovery, experimentation, and a lot of fun. Who knew that terminal customization could offer such ineffable joy? May your endeavors be equally rewarding and filled with the unexpected delight, for, in the end, it’s all about finding beauty in the code—or perhaps a metaphor in our daily routines, nudging us ever closer to a personal utopia.

And with that we're off, our terminals customized, aesthetic boxes checked and Stella ever watchful, purring the whole while.