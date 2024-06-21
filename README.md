<h1 align="center">:pager::satellite: Meshtastic Discord Bot :satellite::pager:</h1>

<p align="center">
  <img src="https://i.imgur.com/V9HLS0E.jpeg">
</p>

<h1 align="center">:warning: This project is still in development! :warning:</h1>
Even though the project is still in development it can be used in its current state.

## Purpose
This Discord bot is used to communicate directly with the [Meshtastic](https://meshtastic.org/) network using a Meshtastic compatable device.

Having a Discord bot directly connected to the Meshtastic network allows users to test their devices and get instant feedback on whether another device has received their message.
It also allows the user to communicate on their local network no matter where they are in the world.

## Screenshots
Coming soon!

## Setup
The following must be established in order for the bot to operate successfully:
- A Meshtastic compatable device must be connected via a serial connection to the device operating the bot.
  - A list of Meshtastic compatable devices can be found [here](https://meshtastic.org/docs/hardware/devices/).
- Update the variables outlined in the next section.

## Variables
Update the following variables in the `config.json` file:
- Replace `YOUR-TOKEN-HERE` with your Discord Bot Token.
  - Instructions on how to create a Discord bot can be found [here](https://discordpy.readthedocs.io/en/stable/discord.html).
- Replace `YOUR-CHANNEL-ID-HERE` with the channel ID from the server the bot will be communicating in.
  - Instructions on how to get the channel ID can be found [here](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID).

Update the following variables in the `main.py` file:
- Line `37`: Replace `CHANNEL0` through `CHANNEL7` with your specific channel names.
- Lines `140 & 326`: Replace `YOUR-TZ` with your timezone.
  - A list of available timezones can be found [here](https://gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568).
- Lines `257-259`: Replace `CHANNEL-NAME-0` and `channelname0` with your specific channel name.
- Lines `263-265`: Replace `CHANNEL-NAME-1` and `channelname1` with your specific channel name.
- Lines `269-271`: Replace `CHANNEL-NAME-2` and `channelname2` with your specific channel name.
- Lines `275-277`: Replace `CHANNEL-NAME-3` and `channelname3` with your specific channel name.
- Lines `281-283`: Replace `CHANNEL-NAME-4` and `channelname4` with your specific channel name.
- Lines `287-289`: Replace `CHANNEL-NAME-5` and `channelname5` with your specific channel name.
- Lines `293-295`: Replace `CHANNEL-NAME-6` and `channelname6` with your specific channel name.
- Lines `299-301`: Replace `CHANNEL-NAME-7` and `channelname7` with your specific channel name.

If the above channel names have been updated, the commands listed in the help menu must also be updated starting on line `205`.

## Commands
Once the above variables have been updated, run the bot using the following commands:
(Note that if you have changed the above channel name variables, the channel commands below will change.)
- `/sendid` followed by the node ID to send a direct message to that node. For example, `/sendid !7c5acfa4`.
- `/sendnum` followed by the node number to send a direct message to that node. For example, `/sendnum 2086326180`.
- `/active` to show a list of active nodes seen in the last 15 minutes.
- `/channel0` to send a message in channel 0.
- `/channel1` to send a message in channel 1.
- `/channel2` to send a message in channel 2.
- `/channel3` to send a message in channel 3.
- `/channel4` to send a message in channel 4.
- `/channel5` to send a message in channel 5.
- `/channel6` to send a message in channel 6.
- `/channel7` to send a message in channel 7.
- `/help` to show a list of available bot commands.

## Credits
The idea for this bot was inspired by the [Meshtastic Discord Bridge](https://github.com/raudette/meshtastic_discord_bridge) created by [raudette](https://github.com/raudette).
