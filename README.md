# Public Bot and Support Server!

<a href="https://discord.gg/dcdev"><img src="https://discord.com/api/guilds/773668217163218944/widget.png?style=banner2"></a>
 
[**Invite the Public Version of this Bot**](https://milrato.milrato.dev) So you don't need to host it by yourself or [join my discord Server](https://discord.gg/dcdev) to get a custom hosted Bot for you!


# Important notes and thank ❤️
This is the sharded version of [Milrato](https://milrato.com) [(CLAN BOT SOURCE CODE - MAIN)](https://github.com/Tomato6966/Multipurpose-discord-bot), it is needed to be used, if ur bot is above 1800 Guilds! *Note, it is suggested to be used, since the beginning, as the db can't get converted from the main to the `sharded_with_mongo` version, and it really doesn't use much memory, it won't work on a replit.com tho, as it needs more resources for the shards....*

If you want you can add a DASHBOARD too, an example how to start it, is listed in `bot.js` at the very bottom!

First of all, thanks for using this Source Code, it was and is a ton of work to create and maintain it!
That's why I'm asking everyone to [**donate a little bit of money**](https://donate.milrato.dev) or if that's not possible, then join my [Discord Server](https://discord.gg/dcdev)!

# Installation Guide 🔥

## ✅ Hosting Requirements

<details>
  <summary>Click to expand</summary>
 
 ### System Requirements
  * min. 300mB Ram, suggested: 500mb (as it takes 300mb on idle
  * 1 Core with min. 2.4ghz
  * min. 150mb Storage, suggested: More, because the DATABASE needs Storage...
  * [nodejs](https://nodejs.org) version 16.6 or higher, i recommend the latest STABLE version
  * [python](https://python.org) version 3.8 or higher, to install the database `enmap` (better-sqlite3)

 ### Recommendations
  * a VPS would be adviced, so you don't need to keep your pc/laptop/raspi 24/7 online! [click here for a debian setup Guide](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/)
  * Check out my Recommended Host: [BERO-HOST](https://bero.milrato.dev) and use code `milrato` for cheap OP VPS (kvm)
  * [Click here for a Direct Order Link](https://bero-host.de/server/prepaid-kvm-rootserver-paket-mieten)

</details>

## 🤖 Bot Requirements

<details>
  <summary>Click to expand</summary>

  **NOTE:** It is suggested to use the [Sharded (&Clustered) version](https://github.com/Tomato6966/Multipurpose-discord-bot/tree/sharded_with_mongo), if u plan on using it for a VERIFIED BOT (on more then 2000 Servers!)
 
  1. Download the [Source Code](https://github.com/Tomato6966/Multipurpose-discord-bot/releases/latest)
     * either by: `git clone https://github.com/Tomato6966/Multipurpose-discord-bot`
     * or by downloading it as a zip from the releases or a branch
  
</details>

## 🎶 Music Requirements

<details>
  <summary>Click to expand</summary>

  *To have your Bot able to play music, you need to connect it to a lavalink Station!*
  *There are many public ones out there for example lavalink.eu*
  An example for a public configuration will be listed down below
   
  1. Make sure `Java 11` is installed on your System!
     * [Click here for a Download for **Linux**](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/3.5.2-java-11)
     * [Click here for a Download for **Windows**](https://downloads.milrato.eu/windows/java/jdk-11.0.11.exe) ​
  2. Download [Lavalink.jar](https://github.com/freyacodes/Lavalink/releases/download/3.4/Lavalink.jar)
     * here is a direct link: https://github.com/freyacodes/Lavalink/releases/download/3.4/Lavalink.jar
     * if you are on linux do this: `wget https://github.com/freyacodes/Lavalink/releases/download/3.4/Lavalink.jar` (prep: `apt-get install -y wget`)
  3. Download [application.yml](https://cdn.discordapp.com/attachments/734517910025928765/934084553751015475/application.yml)
     * Download my example, it's the configuration for the lavalink.jar file!
  4. Now put application.yml and Lavalink.jar in the same folder and start it
     * To start lavalink type: `java -jar Lavalink.jar`
     * Make sure to keep your terminal Open!
     * If you want to use something like `npm i -g pm2` to host it without keeping your terminal open type: `pm2 start java -- -jar Lavalink.jar`
  5. The settings like **password** in application.yml and **port** must be provided in the `botconfig/config.json` of the Bot
     * If you used the default settings, than no adjust ments are needed and it should look like this: 
     ```json
     {
        "clientsettings": {
            "nodes": [
                {
                    "host": "localhost",
                    "port": 2333,
                    "password": "youshallnotpass"
                }
            ]
        }
     }
     ```
  6. You don't want to host your own Lavalink?
     * [Here is a list of many free-to-use Lavalink Servers!](https://lavalink.darrennathanael.com/#how2host)
     * Or just use something like this: 
     ```json
     {
        "clientsettings": {
            "nodes": [
                {
                    "host": "lava.link",
                    "port": 80,
                    "password": "Anything for the Password"
                }
            ]
        }
     }
     ```

</details>

## 🤖 Configuration and Starting

<details>
  <summary>Click to expand</summary>

  **NOTE:** *you can do the exact same configuration inside of the `example.env` File, just make sure to rename it to `.env` or use environment variables!*
 
   1. Check `🎶 Music Requirements` that you started lavalink / use a valid public lavalink station
   2. Fill in all required data in `./botconfig/config.json` **NOTE:** *If you're on replit.com, it is exposed to everyone!(use .env instead)*
   3. Fill in all required data in the `.json` Files in `./social_log/` (`./social_log/streamconfig.json` & `./social_log/twitter.json`), if you want the SOCIAL LOGS to work! (the key `authToken` in streamconfig is not needed to be filled in!)
   4. You can adjust some settings in the other `./botconfig/*.json` Files, **BUT PLEASE __KEEP__ MY CREDITS & ADS!** This is the only way on how my hard work is "revenued"
   5. Now start the bot by typing opening a cmd in that folder and type: `node index.js` or `npm start`
     * If you don't want to keep the terminal open or if you're on linux, check out [pm2 (and my tutorial)](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/4-pm2-tutorial) and type: `pm2 start --name Bot_Name index.js`
  
</details>

## ❓ Where to get which Api-Key(s)

<details>
  <summary>Click to expand</summary>

  **NOTE:** *you can do the exact same configuration inside of the `example.env` File, just make sure to rename it to `.env` or use environment variables!*
 
  1. `./botconfig/config.json`
     * `token` you can get from: [discord-Developers](https://discord.com/developers/applications)
     * `memer_api` you can get from: [Meme-Development DC](https://discord.gg/Mc2FudJkgP)
     * `spotify.clientSecret` you can get from: [Spotify-Developer](https://developer.spotify.com)
     * `spotify.clientID` you can get from: [Spotify-Developer](https://developer.spotify.com)
     * `fnbr` is a FNBR token, which you may get from [FNBRO.co](https://fnbr.co/api/docs) (needed for fnshop)
     * `fortnitetracker` is a FORTNITE TRACKER token, which you may get from [fortnitetracker.com](https://fortnitetracker.com/site-api) (needed for fnstats)
  2. `./social_log/streamconfig.json`
     * `twitch_clientID` you can get from: [Twitch-Developer](https://dev.twitch.tv/docs/api) ([developer-console](https://dev.twitch.tv/console))
     * `twitch_secret` you can get from: [Twitch-Developer](https://dev.twitch.tv/docs/api) ([developer-console](https://dev.twitch.tv/console))
     * `authToken` is not required to be filled in --> will be done automatically
  3. `./social_log/twitter.json`
     * `consumer_key` you can get from: [twitter Developers](https://developer.twitter.com)
     * `consumer_secret` you can get from: [twitter Developers](https://developer.twitter.com)
     * `access_token` you can get from: [twitter Developers](https://developer.twitter.com)
     * `access_token_secret` you can get from: [twitter Developers](https://developer.twitter.com)
  4. `./databaseUri.json`
     * `mongoUri` is your Mongouri, everything should be explained if you need a [**selfhosting Guide CLICK HERE**](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/5-Mongodb-Database) or a free [**MONGODB-ATLAS URL CLICK HERE**](https://www.mongodb.com/atlas/database)
  
</details>


## SUPPORT ME AND MILRATO DEVELOPMENT

> You can always Support me by inviting one of my **own Discord Bots**

[![2021's best Music Bot | Lava Music](https://cdn.discordapp.com/attachments/748533465972080670/817088638780440579/test3.png)](https://lava.milrato.dev)
[![Musicium Music Bot](https://cdn.discordapp.com/attachments/742446682381221938/770055673965707264/test1.png)](https://musicium.musicium.dev)
[![Milrato Multi Bot](https://cdn.discordapp.com/attachments/742446682381221938/770056826724679680/test1.png)](https://milrato.milrato.dev)

# Credits

> If consider using this Bot, make sure to credit me!

- Any Idiot who dosent know how to download the sharded branch, use this. All credits to sussy baka tomato
