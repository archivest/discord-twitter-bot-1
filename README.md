# discord-twitter-bot
Post tweets to Discord Webhook of certain twitter users.  

[![Invite Link](https://discordapp.com/api/guilds/295528852518731786/widget.png?style=shield)](https://discord.gg/Dkg79tc)
[![Build Status](https://api.travis-ci.com/NNTin/discord-twitter-bot.svg)](https://travis-ci.com/NNTin/discord-twitter-bot)
[![Pull Requests](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/NNTin/discord-twitter-bot/pulls)

## Preview

[![](img/gif.gif)](https://discord.gg/Dkg79tc)

## Heroku Deployment

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Remember to [activate](https://i.imgur.com/zOfa0Qm.png) the app. [View the logs here.](https://i.imgur.com/tWBoTuB.png)  
Use this to initially deploy your discord-twitter-bot.

To further configure the bot get Heroku CLI and run launcher.py. (**Warning:** This is not recommended for inexperienced users since a lot of things could go wrong. Troubleshooting support will not be provided.)

```coffeescript
heroku login
heroku create <your heroku app name>
cd <your heroku app name>
git remote add origin https://github.com/NNTin/discord-twitter-bot
git pull origin master
python bot/launcher.py
git add .
git commit -am "updated configuration"
git push heroku
```

This will create a data.json and the bot will ignore any set environment variable.

## YT Video to Heroku Deployment

[![YT Video](https://img.youtube.com/vi/NwPcXBvStSI/0.jpg)](https://www.youtube.com/watch?v=NwPcXBvStSI)

## Normal Setup

(**Warning:** This is only recommended for experienced users who have some basic experience with CLI.)

Get Python >=3.5.3, <3.7

```coffeescript
git clone https://github.com/NNTin/discord-twitter-bot.git
cd discord-twitter-bot      # ^ download the project and cd into it
python3 -m venv venv        # optional virtual environment, recommended
source venv/bin/activate    # only run if you did venv
python3 -m pip install tox  # optional used for testing/troubleshooting/contributing
python3 bot/launcher.py     # configure the bot, this create a config.json
tox                         # only run if you did tox, run the test suite
python3 bot/main.py         # run the bot
```

Once you have set everything up you can run main.py directly. (Useful in combination with systemd, Upstart, PM2, etc.)

![](https://i.imgur.com/TdJahu9.png)

Useful links:
* [Twitter API](https://developer.twitter.com/en/apps)
* [What's a webhook?](https://support.discordapp.com/hc/en-us/articles/228383668-Intro-to-Webhooks)


## Credits
Rokxx for providing the [dota 2 twitter list](https://twitter.com/rokxx/lists/dota-2/members).  
JacobWolf for providing the [twitter lists](https://twitter.com/JacobWolf/lists) for CS:GO, LoL, Overwatch, CoD and SSMB.
