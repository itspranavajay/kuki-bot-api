<h1> <u>KUKI-BOT-API</u> </h1>

### Enjoying kuki-bot-api?


**Developers**:
[Nksama](https://github.com/nksama) -
[Telegram](https://t.me/NksamaX)

[Pranav Ajay](https://github.com/Moezilla)
Discord: MoeZilla#4285
Telegram: PranavAjay

## Simple Example

```
const Kukibot = require("kuki-bot-api");
const kukiai  =  new  Kukibot({name: "Pranav", owner: "MoeZilla"});

kukiai.moe("Hi").then(console.log)
```

## Discord Example:

```
const discord = require("discord.js");

const client = new discord.Client();

const Kukibot = require("kuki-bot-api");

const token = ''; // your discord bot token

const kukiai  =  new  Kukibot({name: "Pranav", owner: "MoeZilla"});

client.on("message", async message => {

  if (message.author.bot) return; 

  let content = message.content;

  kukiai.moe(content).then(reply =>

    message.channel.send(reply, {

             

    })

  ); 

});

client.login(token);
```

## Async / Await

```
const Kukibot = require("kuki-bot-api");
const kukiai  =  new  Kukibot({name: "Pranav", owner: "MoeZilla"});

async function main() {
  const msg = await kukiai.moe("Hi");

  console.log(msg);
}
main();
```

## Instagram Example

``` 
const Insta = require('@androz2091/insta.js');
const client = new Insta.Client();
const fetch = require("node-fetch");
const Kukibot = require("kuki-bot-api");
const kukiai  =  new  Kukibot({name: "Pranav", owner: "MoeZilla"});
 
client.on("messageCreate", async message => {
  if (message.author.id === client.user.id) return;

  message.markSeen();

    let content = message.content;
      if(!content) return;
          kukiai.moe(content).then(r => message.reply(r));
            });

client.login('username', 'password'); 
```
