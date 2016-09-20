CONFIGURE ETHERCHANNEL FOR SERVERS USING INTEL TEAMING (BONDING NICS)

On the Server

1. Install [Intel Advanced Network Services](http://www.intel.com/content/www/us/en/support/network-and-i-o/ethernet-products/000005667.html) software
2. Bond both NICs by creating a team using Type – IEEE 802.3ad Dynamic Link Aggregation
3. Set a static IP address for the new Teamed NIC


On the Cisco Switch

1. `# show etherchannel summary`  - verify your new port channel # doesn't already exist. 
2. `# configure terminal`
3. `# interface <interface#>`
4. `# channel-group <group #> mode active` — configures port for LACP
5. Repeat the above two steps for each port you would like to add to the Etherchannel
6. `# interface port-channel <group #>`
7. `# switchport access vlan <#vlanId>` - optional
7. `# no shutdown`