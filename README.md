# DualServer
Scripts and blacklists for DualServer.

The blacklists are reformatted versions of the unified hosts files maintained by Steven Black:

https://github.com/StevenBlack/hosts

The blacklist file letter codes are as follows:

F: Fake News

G: Gambling

P: Porn

S: Social

The blacklist.txt is only the reformatted unified hosts, blackist-f.txt is the unified hosts and fake news, blacklist-fg.txt is the unified hosts and fake news and gambling, etc.

The unified hosts by itself can block everything from sidebar ads, annoying YouTube video ads, banner ads, and even some invisible embedded analytics trying to gather more information about you. The other files add onto the core unified hosts additional blocks. Once these are configured with your DualServer, these blocks will affect all connected devices using your DualServer DNS service, including laptops, mobile phones, PCs, Macs, Linux, whatever.

Note: A blacklist should be used together with other security measures to be more effective. For instance, a network user could simply change their device's currently configured DNS to get around blacklisting. It's also common for Android devices to automatically use Google DNS as a fallback if they cannot resovle quieries from the DNS servers currently configured on the device either manually or via DHCP. One simple way to make your network more secure would be since your local DNS is on your LAN side, you could therefore configure your network equipment to block requests made by any LAN device other than your server to any server on port 53 on the WAN side to ensure DNS requests can only be made to your local server.

To use these blacklists with DualServer you can either copy and paste their contents under the [DNS_HOSTS] section of the DualServer.ini or simply direct DualServer to the downloaded blacklist file using @blacklist.txt (or whatever the blacklist file name is) under the [DNS_HOSTS] section of the DualServer.ini. Please note, however, if you decide to direct DualServer to a file, the "@" line should be the only uncommented line in the [DNS_HOSTS] section of the DualServer.ini and all entries for the section must then come from the directed file.
