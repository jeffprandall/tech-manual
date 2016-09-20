## Cisco  ##

ROUTERS

`#show ip dhcp binding` - shows all dhcp leases
`# ip access-list resequence <access list name> starting-sequence-number increment` - enable ordering so you can insert rules before specific rules get applied


SWITCHES

`# show mac-address-table | include <mac address>` - remember the mac is formatted as 0000.1111.2222

GENERAL

Reset a device

1. `# enable`
2. `# conf t`
3. `# config-register 0x2102`
4. `# end`
5. `# write erase`
6. `# reload`
7. `# no`

