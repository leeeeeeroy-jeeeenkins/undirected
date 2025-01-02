---
slug: how-to-install-moodle-on-a-linux-server
title: How to Install Moodle on a Linux Server
authors: [undirected]
---


# How to Install Moodle on a Linux Server

Ah, the sweet memory of my first encounter with Moodle. Picture this: a room filled with half-eaten doughnuts, heaps of tangled cables like digital spaghetti, and that one colleague—let’s call him Greg—lecturing about the virtues of open-source while waving a kind of triumphant screwdriver. As it turns out, the task of installing Moodle on our newly acquired Linux server felt daunting, like the final boss in a video game, except instead of dragons, we had server errors and dependency hell. But here we are, wiser, and ready to embark on that journey together, with fewer doughnuts and more know-how. So, let’s chalk up on patience and dive in.

## Step 1: Prep Your Linux Server

Before all else, our trusty server needs some TLC - or, at the very least, an update. Open your terminal, imagine it as the cockpit of a futuristic ship, and input:

```bash
sudo apt update && sudo apt upgrade -y
```

This command makes sure everything's spick and span, just like sweeping the floor before inviting guests—digital spring cleaning if you will. See, Linux is all about housekeeping. Remember Greg singing (badly) in the background about the "Order of Packages"? Yeah, he wasn't wrong.

## Step 2: Install Apache, MySQL, and PHP (AMP)

The sacred AMP trio: Apache, MySQL, and PHP. They make things run smoothly, almost like what coffee does to Monday mornings. Let’s install them with the following command:

```bash
sudo apt install apache2 mysql-server php libapache2-mod-php php-mysql -y
```

Feel free to sip that coffee now. Fun fact: Greg—master of exaggeration and JavaScript puns—once described Apache as "grandpa of the internet." We smiled, pretended we didn't hear him, and pushed onward.

## Step 3: Secure MySQL

Security first, always. It’s like locking the front door before a movie marathon—necessary and sometimes overlooked. Enter into MySQL’s configuration:

```bash
sudo mysql_secure_installation
```

You’ll answer a series of questions. We always chose the secure options—I mean who needs to live on the edge, especially with databases.

## Step 4: Create a MySQL Database and User

Let’s create a database. Think of this as providing Moodle with its own sandbox to play in. Enter MySQL:

```bash
sudo mysql -u root -p
```

After entering your password, run these commands—imagine typing in a secret language (because, essentially, we are):

```sql
CREATE DATABASE moodle DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'moodleuser'@'localhost' IDENTIFIED BY 'yourpassword';
GRANT ALL ON moodle.* TO 'moodleuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

Greg almost ruined it once by naming the user "TheMoodlePoodle," but professionalism prevailed.

## Step 5: Install Additional PHP Extensions

Even the mightiest PHP needs reinforcements. Install some extra PHP extensions—this is Moodle’s demand for a capable helper ensemble.

```bash
sudo apt install php-xml php-intl php-zip php-gd php-curl php-mbstring php-soap -y
```

Never underestimate the power of extensions, like buttons on a coat. They won’t make the coat, but they make it work.

## Step 6: Download Moodle

Finally, the star of the show appears—Moodle itself! Let’s get Moodle from the official website. Move into the `/var/www/html` directory:

```bash
cd /var/www/html
sudo wget https://download.moodle.org/download.php/direct/stable39/moodle-latest-39.tgz
```

We’re practically halfway there! Come to think of it, the first time I did this, I accidentally downloaded a cat GIF instead. Ah, pleasant missteps.

## Step 7: Extract and Assign Proper Permissions

Now, like a kid unwrapping a birthday present, extract Moodle:

```bash
sudo tar -zxvf moodle-latest-39.tgz
```

Next, assign ownership—Moodle won't work without the right permissions; it's like teaching a dog and forgetting the treats:

```bash
sudo chown -R www-data:www-data /var/www/html/moodle
sudo chmod -R 755 /var/www/html/moodle
```

Permissions are your digital keychains, keep them sorted.

## Step 8: Create Moodle Data Directory

Moodle needs its own data closet to store all the bits and bobs away from prying guest eyes:

```bash
sudo mkdir /var/www/moodledata
sudo chown -R www-data:www-data /var/www/moodledata
sudo chmod -R 755 /var/www/moodledata
```

Greg once asked if moodledata was moodle's "pajama pile." Hopefully, you don't ask silly questions like Greg because there are no silly questions when it comes to learning.

## Step 9: Set Up Apache With Moodle

It’s time for introductions—for Apache to meet Moodle. Create a new configuration file:

```bash
sudo nano /etc/apache2/sites-available/moodle.conf
```

Copy this inside—it’s like introducing long-lost friends:

```apache
<VirtualHost *:80>
    ServerAdmin admin@example.com
    DocumentRoot /var/www/html/moodle
    ServerName yourdomain.com
    ServerAlias www.yourdomain.com

    <Directory /var/www/html/moodle/>
        Options +FollowSymlinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

Enable the site and rewrite module to ensure everything talks nicely:

```bash
sudo a2ensite moodle.conf
sudo a2enmod rewrite
sudo systemctl restart apache2
```

A little restart, a new beginning, much like how Greg finally learned to separate personal rock playlists from work presentations.

## Step 10: Final Installation Through Web Interface

The last leg—open your favorite browser and hop to your server's domain or IP address. Follow the instructions onscreen like directions in a treasure hunt.

Enter the database details you set earlier and wait for everything to fall into place. We celebrated this step with virtual confetti the first time—an idea courtesy of Greg, naturally.

## Conclusion

And there we have it. Moodle on a Linux server—a journey filled with enthusiasm, little blunders, and farsighted wisdom from Greg. We journeyed together through the mystical lands of terminal commands and server setups, and emerged victorious.

Remember, each step is a piece of a puzzle. Sometimes you'll struggle, sometimes you'll triumph—but ultimately, you'll learn. Like Greg figuring out Wednesday was Sushi-day, it’s the little revelations that count. Let's toast to open-source, shared learning, and finding joy in the mundane.

Happy Moodling! 🥳

If you have any queries or suggestions, feel free, as always, to drop a pizza emoji in the comments—or better yet, a witty Greg-ism. And remember, technology is best enjoyed with a touch of humanity. Cheers!