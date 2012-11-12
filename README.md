# Wat do?

A bot built using bash, and sic irc by suckless tools.
The bot uses fifo pipes, making it very extensible.

### Dependencies
* bash
* awk
* sic - (source included)

### How to
1. Compile sic.
	1. cd src/sic-1.1
	1. make
	1. cp sic ../../bin
1. Open the bot.conf and fill out the details
1. start the bot by running ./startbot > out&
	* this will pipe bot logs to a file called out and run the bot in the background
	* use "tail -f out" if you want to follow what is being said live. ctrl+c to stop "tail -f"
1. stop the bot by running ./killbot

* Scripts go in the scripts/ dir and need +x to execute. All executable files in the scripts/ dir are currently simply passed args of every string sent by someone in a channel in the form of:
> #channel	: DD/MM/YY hh:mm <name> what the user said

The way scripts work is subject to change as I improve the bot
