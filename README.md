# SOC_AZURE_MICROSOFT_SENTINEL
A home SOC lab made in the cloud using Azure, Microsoft sentinel and a virtual machine

## SUMMARY
*  Created an azure account subscription
* Created a Resource Group, inside of it i have a virtual Network, a subnet and then connected to the
subnet we have a virtual machine
* The virtual machine's Network SEC group or Cloud firewall is completely opened up to the public internet, the virtual firewall inside of the virtual machine is completely opened up to the public as well
*  have a log analytics workspace that operates as a Central log repository,I configured the virtual machine with the Azure monitoring agent to forward all of the security logs into the log analytics workspace
* Created sentinel instance that connects to the log analytics workspace and then inside Sentinel i uploaded a watch list which is basically just a large spreadsheet with geographic information on it with IP blocks
*  Uploaded that watch list and  used the watch list in conjunction with a normal kql query to look up all the failed logins that were happening on my virtual machine and  used the watch list the IP blocks and then the attacker IP address from the logs to figure out where the attackers were coming from like around the world and then  ultimately able to plot them on a map

