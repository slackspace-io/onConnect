onConnect
=========

onConnect is a simple python framework for adding services/actions to be performed when you join/change networks, or based off a change in a monitored file.

For network changes It monitors the arp table, and if it finds a matching configuration for a MAC on the network, it will apply it. This method for tracking/configuration may change, but for now it works with known limitations. You can not have two MAC addresses on the network with configuations defined, it will default to making No Change.

Volume is the only option under wireless, and could be accomplished using the normal command method as well, it takes a value between 1-100 that will set the % volume via amixer. Otherwise youmust add custom commands to run after a network change. You may add custom commands in the format of 'custom.$name: $cmd' under the network configurations. It will run the command as root, and continue on. No validation of success, or waiting for the process. 

You may also configure a [File:$name] configuration which you indicate a file to be polled frequently. On change of the value, the daemon can run a command or script if the value matches or fails to match the set value.

Please check out the included example conf file.

First time sharing something with the public, any advice welcome 

Updated Post: http://jpyth.com/?p=158 
Initial Post: http://jpyth.com/?p=123
