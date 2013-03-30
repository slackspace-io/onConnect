onConnect
=========

onConnect is a simple python framework for adding services/actions to be performed when you join/change networks. It monitors the arp table, and if it finds a matching configuration for a MAC on the network, it will apply it. This method for tracking/configuration may change, but for now it works with known limitations. You can not have two MAC addresses on the network with configuations defined, it will default to making No Change.

Volume is the only 'option', and takes a value between 1-100 that will set the % volume via amixer.

Otherwise you may add custom commands in the format of 'custom.$name: $cmd'. It will run the command as root, and continue on. No validation of success, or waiting for the process. 

First time sharing something with the public, any advice welcome. Post about it: http://jpyth.com/?p=123


