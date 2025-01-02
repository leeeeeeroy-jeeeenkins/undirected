---
slug: how-to-migrate-moodle-to-a-new-server
title: How to Migrate Moodle to a New Server
authors: [undirected]
---


# How to Migrate Moodle to a New Server

I remember the first time we decided to move our Moodle server. Oh boy, what a day that was! As usual, it was a case of 'the clock is ticking, and the students and teachers need it up by Monday.' It was the perfect mix of chaos and excitement—you know, the kind that makes your palms sweat and your brain feel like it’s doing gymnastics. But let me take you through our journey, step-by-step, while also throwing in a dash of humor and common sense that keeps us all sane.

## The Prelude to Migration

It all started in the cramped IT office, where the smell of stale coffee lingered. Our team was huddled around a whiteboard. "Why are we doing this again?" Sarah, my ever-inquisitive colleague, asked. "Because," I replied with a smirk, "our server is so old it remembers when Moodle was a fancy pie in the sky."

### Step 1: Inventory and Planning

Before we started the migration, we needed to get our ducks in a row. It was like preparing for a great journey—one doesn’t simply wake up and climb Everest. We made a comprehensive list of everything in our Moodle database, like courses, plugins, themes, and sneaky customizations that might have slipped under the radar. It was like packing for a vacation, minus the sunblock.

**Why Plan?** Well, without a plan, we'd be lost—and let me tell you, no one wants to be stuck in the labyrinth that is server logistics.

## The Backup Dance

One cannot stress enough the importance of backups. It’s like packing spare underwear for a trip: you hope you won’t need them, but man, if you do…

### Step 2: Backup Everything

"Backup. Backup. Backup." Those words became our team’s mantra. We backed up Moodle's site data and database. It was a tense affair—nailing that perfect backup is like hitting the save button on a term paper at 4 a.m.—you ain't sleeping till it's done.

Here’s what we did:

```bash
# Backup Moodle database
mysqldump -u moodleuser -p moodle_db > moodle_db_backup.sql

# Backup Moodle data files
tar -cvzf moodle_data_backup.tar.gz /moodledata
```

### Folks, Don't Forget

- **Database**: The heart of Moodle, where all the magic happens.
- **Moodledata**: Your digital attic, full of course files and cached info.

## The Big Switch

Ok, so now came the moment of bravery. Like crossing a rickety bridge, our move to the new server was teetering on the edge of thrilling and terrifying.

### Step 3: Set Up the New Server

We unwrapped our new server. "It smells better than a new car," Tom quipped, which was bizarrely accurate. Then we installed the necessary environment—think of it as setting up a new home with the right foundations.

- **Apache/NGINX**: Like the nice garden path leading to your house.
- **PHP**: The wiring your gadgets depend on.
- **MySQL/MariaDB**: The pantry that holds your edibles—or information, in our case.

#### Commands for the Tech-Savvy

Here's a snippet for LAMP setup, should you find it handy:

```bash
# Install Apache
sudo apt update
sudo apt install apache2

# Install PHP
sudo apt install php libapache2-mod-php php-mysql

# Install MySQL
sudo apt install mysql-server
# Secure your MySQL
sudo mysql_secure_installation
```

## The Transfer Tango

Transferring data is like moving furniture to a new house. It's cumbersome, yet it needs to be done with care, lest you scratch the floor—or in our case, mess up the database.

### Step 4: Transfer the Backup

We connected to our new server. The process was a mix of commanding syntax and praying to the Tech Gods for everything to go smoothly.

- **Upload your backup files**: You’ll feel like a digital Santa Claus, bringing precious gifts to their new home.
  
```bash
# Transfer using SCP
scp /path/to/moodle_db_backup.sql username@newserver:/path/to/destination
scp /path/to/moodle_data_backup.tar.gz username@newserver:/path/to/destination
```

- **Extract and restore**: The operation required precision—if we fumbled here, everything could unravel.

```bash
# Restore Moodle database
mysql -u moodleuser -p new_moodle_db < moodle_db_backup.sql

# Extract data files
tar -xvzf moodle_data_backup.tar.gz -C /new/moodledata
```

## The Configuration Conundrum

With everything in place, it was time to adjust the settings, make sure our Moodle was comfortable in its fresh digs, like adjusting curtains and testing the light switches in a new apartment.

### Step 5: Configure Moodle

Ah, `config.php`—the intimidating gatekeeper. Sarah bravely volunteered to tackle it, navigating its innards with all the focus of a bomb defuser. 

- **Update database details**: Make the new house your home by changing the address, in this case, database credentials.
  
```php
$CFG->dbtype    = 'mysqli'; // Or whatever database driver you're using
$CFG->dbhost    = 'localhost';
$CFG->dbname    = 'new_moodle_db';
$CFG->dbuser    = 'moodleuser';
$CFG->dbpass    = 'yourpassword';
```

- **Update data root**: Changing the path’s like rearranging furniture. You know where things should go, you just need to do it.

```php
$CFG->dataroot  = '/new/moodledata';
```

## Testing the Waters

Once all was said and done, we held our collective breaths and powered on the new server—much like waiting for the cake to bake without peeking inside the oven.

### Step 6: Testing and Tweaking

"You think it’ll work?" Tom asked, half-joking, half-terrified. We visited the site URL. It loaded—hallelujah! But like any good story, there were a few hiccups. 

We navigated through the site: enrolled in courses, checked forum posts, made sure every cog was spinning smoothly.

If something was amiss, we rectified it swiftly, like painting over a blotch on a freshly decorated wall.

## The Victory Lap

And finally, the migration was complete. It was an arduous journey with learning curves steeper than Everest itself, but the end result was worth every migraine, every midnight coffee.

### Final Thoughts

Migrations like these remind us not only of the power of technology but also the patience and tenacity one needs when dealing with such behemoths. Our Moodle was now faster, more robust, and ready for whatever the educational world wanted to throw at it.

In the end, moving Moodle wasn't just about transferring bytes and bits. It was a journey—a quest even—that brought us closer as a team.

And it left us with stories to tell, which, like all good tales, have their fair share of humor, stress, and triumph.

Needless to say, we celebrated. There may or may not have been cake—and maybe a bottle or two of something fizzy.

Now, dear reader, it's your turn. May your migration be smooth, your backups secure, and your journey be full of discovery. Cheers to the wild ride that is Moodle migration!