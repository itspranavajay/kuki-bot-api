<h1>KUKI-BOT-API</h1>

### Enjoying kuki-bot-api?


**Developers**:
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

const kukiai  =  new  Kukibot({name: "Pranav", owner: "MoeZilla"});

client.on("message", async message => {

  if (message.author.bot) return; 

  let content = message.content;

  kukiai.moe(content).then(reply =>

    message.channel.send(reply, {

             

    })

  ); 

});

client.login(token here);
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
