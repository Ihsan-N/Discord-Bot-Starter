# Discord-Bot-
A basic discord bot 
# Basic Discord.js Bot

__Installation__

Use `npm init` and it will create a package.json file

```sh
npm init
```

Now Make a File called `index.js` and type `npm i discord.js` in the terminal.

```sh
npm i discord.js
```

Get your bot token from **[Discord Developer Portal](https://discord.com/developers/docs)**

```javascript
const Discord = require("discord.js");
const client = new Discord.Client({
  intents: [
    "GUILDS",
    "GUILD_MESSAGES",
  ],
});



client.on('ready', () => {
  console.log("I'm in");
  console.log(client.user.username);
});

let prefix = "!";// or use the prefix that you want 

client.on("messageCreate", (message) => {

  if (!message.content.startsWith(prefix) || message.author.bot) return;
 
  if (message.content.startsWith(prefix + "ping")) { // ping command
    message.channel.send("pong."); // responds by sending pong 
 
  }
});

client.login(token)//your discord bot token from Developer Portal
```
To Start the Bot Use `node index.js` in the terminal.

```sh
node index.js
```
