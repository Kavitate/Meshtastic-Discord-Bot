<h1 align="center">:pager::satellite: Meshtastic Discord Bot :satellite::pager:</h1>

<p align="center">
  <img src="https://i.imgur.com/oFp9Hk0.jpeg">
</p>

## Purpose
This Discord bot is used to communicate directly with the [Meshtastic](https://meshtastic.org/) network using a Meshtastic compatable device.

Having a Discord bot directly connected to the Meshtastic network allows users to test their devices and get instant feedback on whether another device has received their message.
It also allows the user to communicate on their local network no matter where they are in the world.

## Screenshots

<p float="left">
  <img align="center" src="https://i.imgur.com/gOznvfX.png" width="350" height="175"/>
  <img align="right" src="https://i.imgur.com/NiL2Ow2.png" width="350" height="175"/>
</p>

<p float="left">
  <img align="center" src="https://i.imgur.com/jCrQDW9.png" width="350" height="175"/>
  <img align="right" src="https://i.imgur.com/R8iTtPF.png" width="350" height="175"/>
</p>

<p float="left">
  <img align="center" src="https://i.imgur.com/84trvDK.png" width="950" height="300"/>
</p>

## Setup
The following must be established in order for the bot to operate successfully:
- A Meshtastic compatable device must be connected via a serial connection to the device operating the bot.
  - A list of Meshtastic compatable devices can be found [here](https://meshtastic.org/docs/hardware/devices/).
- Update the variables outlined in the next section.

## Variables
Update the following variables in the `config.json` file:
- Replace `YOUR_DISCORD_BOT_TOKEN` with your Discord Bot Token.
  - Instructions on how to create a Discord bot can be found [here](https://discordpy.readthedocs.io/en/stable/discord.html).
- Replace `YOUR_DISCORD_CHANNEL_ID` with the channel ID from the server the bot will be communicating in.
  - Instructions on how to get the channel ID can be found [here](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID).
- Replace `YOUR_TIME_ZONE` with your zime zone.
  - A list of available timezones can be found [here](https://gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568).
- Replace all channel names with the channel names you've setup on your radio.
  - All channel names must be unique!
  - If you do not use all seven channels, that's fine. Just leave the unused ones as they are or remove its entire entry from the `config.json` file.

## Commands
Once the above variables have been updated, run the bot using the following commands:

Note that if you have changed the above channel name variables in the `config.json` file, the channel commands below will change.
- `/sendid` followed by the node ID to send a direct message to that node. For example, `/sendid !7c5acfa4`.
- `/sendnum` followed by the node number to send a direct message to that node. For example, `/sendnum 2086326180`.
- `/active` to show a list of active nodes seen in the last 15 minutes.
- `/YOUR_CHANNEL_0` to send a message in channel 0.
- `/YOUR_CHANNEL_1` to send a message in channel 1.
- `/YOUR_CHANNEL_2` to send a message in channel 2.
- `/YOUR_CHANNEL_3` to send a message in channel 3.
- `/YOUR_CHANNEL_4` to send a message in channel 4.
- `/YOUR_CHANNEL_5` to send a message in channel 5.
- `/YOUR_CHANNEL_6` to send a message in channel 6.
- `/YOUR_CHANNEL_7` to send a message in channel 7.
- `/help` to show a list of available bot commands.

## Quirks
I've noticed that after running the bot for months on end there are times where it would stop pulling messages unti I would reboot the bot and radio.

I'm not sure if this is specific to the radio itself or not.
  - Currently my bot is running utilizing a Lilygo T-Beam Supreme.

To get around this issue I have set the bot up as a service on a timer to reboot every night.
Since I have made this change I have not noticed any messages being hung.

## Credits
The idea for this bot was inspired by the [Meshtastic Discord Bridge](https://github.com/raudette/meshtastic_discord_bridge) created by [raudette](https://github.com/raudette).
