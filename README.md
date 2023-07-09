cgminer-monitor

Simple monitor script for cgminer in python. Console display, http server, email alerts. No additional modules required.

Tested with python 2.7.2 and cgminer 3.2.0.

usage: cgminer-monitor.py [command] [parameter]


## Monitor mode
cgminer-monitor.py
 - Monitors cgminer by checking a few critical values
 - Emails if something is wrong
 - Restarts cgminer if the GPU is sick or dead
 - Runs a dead simple http server that only serves a page with the results of the monitor (identical to the console output with a nice display)
 - Monitors MMFCE pools and display the current balance in their currencies
 - Could support multi-gpus very easily (see comment in the code)
 - CTRL+C to stop everything

## Command mode
cgminer-monitor.py somecommand someoptionalparameter
 - Ouputs the results returned by cgminer miner and exits
 - Examples:
 	- cgminer-monitor.py summary
 	- cgminer-monitor.py gpu 0
 	- See cgminer's API-README for all available commands