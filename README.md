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

<p float="left">
  <img align="center" src="https://i.imgur.com/gOznvfX.png" width="450" height="250"/>
  <img align="right" src="https://i.imgur.com/NiL2Ow2.png" width="450" height="250"/>
</p>

<p float="left">
  <img align="center" src="https://i.imgur.com/jCrQDW9.png" width="450" height="250"/>
  <img align="right" src="https://i.imgur.com/R8iTtPF.png" width="450" height="250"/>
</p>

<p float="left">
  <img align="center" src="https://i.imgur.com/84trvDK.png" width="1050" height="400"/>
</p>

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
- Line `146`: Replace `YOUR-TZ` with your timezone.
  - A list of available timezones can be found [here](https://gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568).
- Lines `267-272`: Replace `CHANNEL-NAME-0` and `channelname0` with your specific channel name.
- Lines `277-282`: Replace `CHANNEL-NAME-1` and `channelname1` with your specific channel name.
- Lines `287-292`: Replace `CHANNEL-NAME-2` and `channelname2` with your specific channel name.
- Lines `297-302`: Replace `CHANNEL-NAME-3` and `channelname3` with your specific channel name.
- Lines `307-312`: Replace `CHANNEL-NAME-4` and `channelname4` with your specific channel name.
- Lines `317-322`: Replace `CHANNEL-NAME-5` and `channelname5` with your specific channel name.
- Lines `327-332`: Replace `CHANNEL-NAME-6` and `channelname6` with your specific channel name.
- Lines `337-342`: Replace `CHANNEL-NAME-7` and `channelname7` with your specific channel name.

If the above channel names have been updated, the commands listed in the help menu must also be updated starting on line `211`.

## Commands
Once the above variables have been updated, run the bot using the following commands:
(Note that if you have changed the above channel name variables, the channel commands below will change.)
- `/sendid` followed by the node ID to send a direct message to that node. For example, `/sendid !7c5acfa4`.
- `/sendnum` followed by the node number to send a direct message to that node. For example, `/sendnum 2086326180`.
- `/active` to show a list of active nodes seen in the last 15 minutes.
- `/channelname0` to send a message in channel 0.
- `/channelname1` to send a message in channel 1.
- `/channelname2` to send a message in channel 2.
- `/channelname3` to send a message in channel 3.
- `/channelname4` to send a message in channel 4.
- `/channelname5` to send a message in channel 5.
- `/channelname6` to send a message in channel 6.
- `/channelname7` to send a message in channel 7.
- `/help` to show a list of available bot commands.

## Credits
The idea for this bot was inspired by the [Meshtastic Discord Bridge](https://github.com/raudette/meshtastic_discord_bridge) created by [raudette](https://github.com/raudette).
