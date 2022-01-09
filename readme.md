<p align="center">
	<h1 align="center"> Telegram Bot </h1>
</p>

## Description

This is a Telegram Bot template that can used as template personal bot

## Telegram Api Token and username

1. First you will need create a telegram account and then search for the `@BotFather`. Then type the command - `/newbot`

1. After that given the `username` and save this username as it will be required later.

1. The `@BotFather` will give you the API Token for your bot.

## Getting started with the Telegram-Bot

1. The project requires a `config.yaml` file. There are two ways to generate the same.

    - Manually  - create a `config.yaml` in the directory where `bot.py` lies, with the following contents.

        ```yaml
            token:  <put your bot <API token> here>
            username: <put the bot <username> here>
            bot_admin: <bot admin username>
            trusted_users:  <any trusted user>
        ```

    - From the command Line

        If you have not created the yaml file, you can also generate one from the command line. When you start the app without a `config.yaml` in the project directory, the command line will ask for few tokens( Those you have acquired from `@BotFather`)

        Just give the tokens and username to the command line and it will generate the yaml file for you.

1. The `bot.py` will also generate the saved folder inside the project directory.

    - Here all the files will be stored that the trusted_users and admins upload.

## Bot Function

#### There are 3 levels of privilage and has a bottom to top inclusive nature:
1. Admin - AU
1. Trusted user - TU
1.  Non-Trusted user - U

|command|Description|Privilage|
|:---|:---|:---:|
|   /start |   Welcome message |    U   |
|   /help  |   help message    |   U   |
|   /contact    |   Bot Admin Info  |   U   |
|   /list   |   List all the saved files    |   U   |
|   /ig_dp  |   Download Instagram DP   |   U   |
|   /print  |   Print a saved file  |    TU  |
| add_trusted `<username>` | Add new trusted user to list| AU|
| add_admin `<username>` | Add new bot admin to list| AU|
|   upload a file | Uploads and saves the file | TU |


## Instructions to run:

- Change working directory to project directory: `cd /path/to/telegram_bot`
- Install the requirements: `$pip3 install -r requirements.txt`
- Run the bot: `$python3 bot.py`
- Stop the bot: `ctrl + c`