# AutoBW
AUTO Bandwidth: Set QoS upload/download speeds on Asus Routers running Merlin firmware

Please post questions here:
[SNBforums](https://www.snbforums.com/threads/autobw-automatically-set-qos-bandwidth-using-spdmerlin.63067/)

Set QoS upload/download speeds using Ookla speedtests and spdMerlin
Requires bc and spdMerlin (v3.3.2 or later)

Some of the functionality here was either taken directly or adapted from the FreshJr_QOS script

	v1.0 (3/25/2020): Initial Release
	
	v1.1 (4/01/2020): Complete rewrite
		-No longer requires bash
		-Checks that bc is installed & QoS enabled & upload traffic is directed to unthrottled class
		-No need to stop/start QoS
		-Class rates/ceils are scaled
	
	v1.2 (4/03/2020): More changes
		-Check for spdMerlin
		-Formatted logger message concerning new BW
		-Check for appropriate iptable rules that ensure spdMerlin traffic in unaffected by QoS
	
	v1.3 (4/03/2020): Changed an important check
		-Check for spdMerlin v3.3.2 or greater to ensure that QoS will not interfere with calculated speeds
	
	v1.4 (4/03/2020): Added option for automatic updates
		-If turned on, check for updates. If found then update.
	
	v1.5 (4/05/2020): Now handles VPN and Gbps|Mbps|Kbps rates/ceils
		-Use VPN values, if defined (thanks maghuro)
		-Handle rate/ceil units other than just Kbps (thanks peepsnet)
