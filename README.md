# Telegram Companion

 ![](https://img.shields.io/github/forks/nitanmarcel/TelegramCompanionV2.svg?style=social) ![](https://img.shields.io/github/stars/nitanmarcel/TelegramCompanionV2.svg?style=social) ![](https://img.shields.io/github/watchers/nitanmarcel/TelegramCompanionV2.svg?style=social)
 

> TelegramCompanion is simple userbot for Telegram to make your time spent on telegram more enjoyable. It runs in the background of your PC or server and gives you some new and usefull features!

## Table of contents

-   [Setup](#Setup)
-   [Configuration](#Configuration)
-   [Features](#Features)
-   [Plugins](#Plugins)
-   [Support](#Support)
-   [Donate](#Donate)
-   [License](#License)


## Setup

- Install all the apt apt dependencies

```bash
sudo apt install python3.7 python3.7-dev
```

- Clone the repo

```bash
git clone https://github.com/nitanmarcel/TelegramCompanion
```

- Cd to the cloned folder and install all the requirements
```bash
pip3 install -r requirements.txt
```

## Configuration
> There are two ways to setup userbot's config variables. You can use env variables or create a config.env file!

The following config variables are supported:

- API_ID (**required**) - The application id from https://my.telegram.org/apps
- API_HASH (**required**) - The application hash from https://my.telegram.org/apps
- CMD_PREFIX (**optional**) - The prefix to be used for calling commands! Defaults to `.`
- DB_URI (**optional**) - The url of the postgresql database. If there's no url given the companion will create a session file to log in to telegram instead of saving the session in the postgresql database. Also future sql modules won't work!
- SESSION_NAME (**optional**) - The name of the session to be used for the companion! Defaults to `companion`! After you logged in with this session name you can change the variable to switch between multiple accounts!
- ANTI_SPAM (**optional**) - Set to anything to enable spam protection on private messages

## Features

Telegram Companion brings some small improvements and new features to any Telegram Client

Every command follows tgbot's syntax but instead of `/<command>` we use `.<command>` (This can be changed in the config.env file or using env variables. See [Configuration](#Configuration))

## Plugins

Plugins allow users to create their own plugins in a official [repo](https://github.com/nitanmarcel/TgCompanionPlugins) or on their own repo, so the user can install them using `python3 -m tg_companion.pluginmanager --install` `<pluginname>` or `python3 -m tg_companion.pluginmanager` `<githubusername>` `<reponame>` `pluginname` if using a unofficial repo!

To uninstall a plugin run `python3 -m tg_companion.pluginmanager --remove` `<pluginname>`

Check [TgCompanionPlugins](https://github.com/nitanmarcel/TgCompanionPlugins) repo for more informations.


**Install plugins on heroku:**

If you are using heroku like servers you can install any plugins by creating a `plugins.txt` file and add the plugins you want to install there. (Just like you do with the pip requirements!)

## Support

You can get support in our official telegram group: https://t.me/tgcompanion

## Donate

It took a lot of work and white nights for me to do this user-bot and make it look less like another Bot that you control and more a part of your telegram client.
I know is not perfect but I'm trying my best and if you enjoy this UserBot and you want to help me you can buy me a beer using [PayPal](https://www.paypal.me/marcelalexandrunitan). Any donation will help. Thanks and I hope you enjoy my Companion!


## License
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

This code is licensed under [GPL v3](LICENSE).