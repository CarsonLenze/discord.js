<div align="center">
  <br />
  <p>
    <a href="https://discord.js.org"><img src="https://discord.js.org/static/logo.svg" width="546" alt="discord.js" /></a>
  </p>
</div>

## About

Self-bot friendly version of discord.js v13, a powerful [Node.js](https://nodejs.org) module that allows you to easily interact with the
[Discord API](https://discord.com/developers/docs/intro). 

- Object-oriented
- Predictable abstractions
- Performant
- 100% coverage of the Discord API

## This version's caveats
- Not everything is tested, if something doesn't work open an issue.
- Intents aren't needed, they are all enabled by default.
- All the slash commands stuff won't work for obvious reasons.
- Sharding isn't supported.
- This doesn't work with bot tokens anymore.
- The useragent is hardcoded to Chrome/92.0.4515.131.

## Installation

**Node.js 16.6.0 or newer is required.**  

```sh-session
npm install git+https://github.com/GiorgioBrux/discord.js.git
```

### Optional packages
> Not tested
- [zlib-sync](https://www.npmjs.com/package/zlib-sync) for WebSocket data compression and inflation (`npm install zlib-sync`)
- [erlpack](https://github.com/discord/erlpack) for significantly faster WebSocket data (de)serialisation (`npm install discord/erlpack`)
- [bufferutil](https://www.npmjs.com/package/bufferutil) for a much faster WebSocket connection (`npm install bufferutil`)
- [utf-8-validate](https://www.npmjs.com/package/utf-8-validate) in combination with `bufferutil` for much faster WebSocket processing (`npm install utf-8-validate`)
- [@discordjs/voice](https://github.com/discordjs/voice) for interacting with the Discord Voice API

## Example usage

```js
const { Client } = require('discord.js');
const client = new Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});


client.login('token');
```

