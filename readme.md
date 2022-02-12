<p align="center">
	<h1 align="center"> Telegram Bot </h1>
</p>

## Description

This is a telegram bot that can be used as a template for personal telegram bot.

## Telegram API Token Generation

1. First you will need to create a personal telegram account and then search for `@BotFather`. Then type the command - `/newbot`

1. After that, enter the `username` for the bot.

1. The `@BotFather` will give you the API Token for the bot.

## Getting started with the Telegram-Bot

1. Make sure you are in the project directory: 

        cd /path/to/telegram_bot
        
2. Install the requirements: 

        pip3 install -r requirements.txt

3. Creating `config.yaml` file manually - This step could be skipped as running the bot without this file will automatically generate it for you.

```yaml
token: <put the bot token here>
bot_admin: <bot admin username>
trusted_users: <trusted user's username>
```
The `bot.py` will also generate the `saved` folder inside the project directory. 
All the files that the trusted_users and admins send to the bot via telegram chat will be stored here.

4. Run the bot: 

        python3 bot.py

5. To Stop the bot: 

        ctrl + c

## Bot Functions

#### There are 3 levels of privileges for the functions:
1. General User - U
1. Trusted User - TU
1. Admin - AU

|Function Name|Description|Privilege|
|:---|:---|:---:|
|   /start |   Welcome message |    U   |
|   /help  |   help message    |   U   |
|   /contact    |   Bot Admin Info  |   U   |
|   /ig_dp `<insta username>` |   Download Instagram DP   |   U   |
|   /list   |   List all the saved files    |   TU   |
|   /print `<S.No. of file in list>` |   Print a saved file  |   TU  |
|   /print_range `<S.No. of file>` `<Range>` |   Print a range of pages from a saved file  |   TU  |
|   Upload a file | Downloads and saves the file locally | TU |
| /add_trusted `<username>` | Add new trusted user to list | AU |
| /add_admin `<username>` | Add new bot admin to list | AU |
