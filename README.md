# Music-bot

A complete code for a discord music bot 🎧

Looking for a code for a music bot? This fully open-source code is made for your project!


### ⚡ Configuration

Open the configuration file located in the main folder `config.js`.

```js
module.exports = {
    app: {
        token: 'bot token goes here',
        playing: 'by Resonance ❤️',
        global: true,
        guild: 'your server ID goes here',
        ExtraMessages: false,
        loopMessage: false,
},
    opt: {
        DJ: {
            enabled: false,
            roleName: '',
            commands: []
        },
        maxVol: 100,
        spotifyBridge: true,
        volume: 75,
        leaveOnEmpty: true,
        leaveOnEmptyCooldown: 60000,
        leaveOnEnd: true,
        leaveOnEndCooldown: 60000,
        discordPlayer: {
            ytdlOptions: {
                quality: 'highestaudio',
                highWaterMark: 1 << 25
            }
        }
    }
};
```

Basic configuration

- `app/token`, the token of the bot available on the [Discord Developers](https://discordapp.com/developers/applications) section
- `app/playing`, the activity of the bot
- `app/global`, whether the commands will work on all servers or just one (if global they might take up to an hour to show up)
- `app/guild`, the guild the slash command will be loaded to (this only applys if global is set to false)
- `app/ExtraMessages` will increesse the amount of bot spam, while you get more infomation (not recommended) 
- `opt/loopMessage`, if the message that a music is played should be sent when it is looped

DJ mode configuration

- `opt/DJ/enabled`, whether the DJ mode should be activated or not 
- `opt/DJ/roleName`, the name of the DJ role to be used
- `opt/DJ/commands`, the list of commands limited to members with the DJ role

Advanced configuration (only change if you know what you are doing)

- `opt/maxVol`, the maximum volume that users can define
- `opt/spotifyBridge`, takes spotify songs/playlists and searches it on youtube and plays it (highly recommended)
- `opt/volume`, is the defaul volume the queue will start at
- `opt/leaveOnEmpty`, if the bot will leave when the queue is empty
- `opt/leaveOnEmptyCooldown`, the cooldown before the bot leaves when the queue is empty
- `opt/leaveOnEnd`,  if the bot will leave on finishing the queue
- `opt/leaveOnEndCooldown`, the cooldown before the bot leaves on finishing the queue
- `opt/discordPlayer`, options used by discord-player

### 📑 Installation
To use the project correctly you will need some tools.

WARNING: You MUST use Node.js version under 18.17, otherwise, you will encounter major compatibility issues.

[FFmpeg](https://www.ffmpeg.org) to process audio

[Node JS](https://nodejs.org/en/) (v18.17) or older for environment

[yarn](https://yarnpkg.com/getting-started/usage) for package management


Now in your terminal run the following commands assuming you are in the same directory as the project.

`npm install`
 and then run the command 
`node main.js`)

and Done, your bot should be running!

Realized with ❤️ by [Ayushman](https://github.com/circuit-overtime).

Please do not withdraw the license and keep the credits on this project. 
