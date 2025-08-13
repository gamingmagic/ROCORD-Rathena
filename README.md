# Discord Channel
- Link: [https://holicnode.com/discord](https://holicnode.com/discord)

# ROCORD-Rathena
1. Apply Diff https://github.com/gamingmagic/ROCORD-Rathena/commit/ceb7b5e42db5c690c7a8e86cf225c7ccc5af6ba4
2. Install NPM
3. Run rathena and Discord Bot

# Discord TCP Relay Bot

A Node.js-based Discord bot that relays messages between a Rathena server and Discord channels using webhooks.

## Features

- Listens to TCP connections and forwards messages to Discord channels.
- Supports multiple languages and different webhooks for each language.
- Provides real-time updates of server messages to designated Discord channels.

## Requirements

- Node.js v12.x or higher
- npm (Node Package Manager)
- A Discord bot token
- Discord webhooks for each language/channel

## Installation

1. **Clone the repository:**

    ```sh
    git clone https://github.com/gamingmagic/ROCORD-Rathena.git
    cd ROCORD-Rathena/discordbot/
    ```

2. **Install the dependencies:**

    ```sh
    npm install
	npm install discord.js axios
    ```

3. **Configure the bot:**

    Edit the `index.js` file and replace the placeholders with your actual Discord bot token and webhook URLs:

    ```javascript
    const BOT_TOKEN = 'YOUR_ACTUAL_BOT_TOKEN';
    const MainWebhookURL = 'YOUR_MAIN_WEBHOOK';
    const englishWebhookURL = 'YOUR_ENGLISH_WEBHOOK';
    const filipinoWebhookURL = 'YOUR_FILIPINO_WEBHOOK';
    const malaysianWebhookURL = 'YOUR_MALAYSIAN_WEBHOOK';
    const indonesianWebhookURL = 'YOUR_INDONESIAN_WEBHOOK';
    const brazilWebhookURL = 'YOUR_BRAZIL_WEBHOOK';
    ```

## Usage

1. **Start the bot:**

    ```sh
    node index.js
    or use PM2 for robust connection.
    ```

2. **Bot commands:**

    - To send a reply message, use the command in Discord:
      
      ```
      /reply <username> <message>
      ```

    - To request something, use the command in Discord:
      
      ```
      @request <message> -- Ingame Commands
      ```
	- Whisper Channel - Ingame
	  ```
	  #main
	  #enlishg
	  #support
	  #brazil
	  #Filipino
	  ```
![image](https://github.com/gamingmagic/ROCORD-Rathena/assets/53240858/777f298f-a17e-4ff8-a3ac-7995c4757577)


https://github.com/gamingmagic/ROCORD-Rathena/assets/53240858/26627763-2044-4f3a-93d6-7e3f2cdce9f4


3. **TCP Server:**

    The bot starts a TCP server on the specified IP and port. You can send messages to the server, and it will relay them to the appropriate Discord channels based on the prefixes in the message content.

## Bot Configuration

- **Activity Status:**

    The bot sets its activity status every 5 minutes. You can customize this status in the `bot.js` file:

    ```javascript
    setInterval(() => bot.user.setPresence({
        activity: { name: 'domain.com/wiki' },
        status: 'online'
    }), 300000); // 5 minutes
    ```

## Contribution

Feel free to fork this repository and submit pull requests. Contributions are welcome!

## Original Author

Normynator

---

*This project is maintained by [GamingMagic](https://github.com/gamingmagic).*
