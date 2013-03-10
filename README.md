# Wat do?

A bot built using bash, and sic irc by suckless tools. The bot uses fifo pipes, making it very extensible, and bash built-ins, making it reasonably snappy. Nearly everything about this bot can be changed on the fly.

### Dependencies
bash, sic (source included), fortune-mod (optional), tail (optional)

### How to
1. Compile sic.
	1. cd conf/src/sic-1.1
	2. make
	3. cp sic ../../bin
2. Open the conf/bot.conf and fill out the details
3. start the bot by running ./startbot
	* this will pipe bot logs to a file called out in conf/pipes/ and run the bot in the background
	* use "tail -f conf/pipes/out" to monitor bot events.
4. stop the bot by running ./ctrlbot kill

### Scripts
Scripts go in the conf/scripts/ dir and need +x to execute. See the example script conf/scripts/fortune for a simple tutorial on how to write scripts.

Use '!reload' in a channel or PM to synchronize modifications made to the bot, including scripts added/removed/modified, and changes to the ctrlbot file. Most of the bot's behavior is defined in the ctrlbot file. Modification to the startbot file is usually unnecessary, and will require a restart of the bot to take effect.

### To-do:
* Permissions
