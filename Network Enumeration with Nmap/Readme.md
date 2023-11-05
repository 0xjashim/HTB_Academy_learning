#Host Discovery using Nmap
`nmap 10.129.2.0/24 -sn -oA tnet | grep for | cut -d" " -f5`
Breakdown the command

-10.129.2.0/24 	  # Target network range.
-sn 	            # Disables port scanning.
-oA               # tnet 	Stores the results in all formats starting with the name 'tnet'.

#Host Discovery from the host lists
`nmap -sn -oA tnet -iL hosts.lst | grep for | cut -d" " -f5`


#
`nmap 10.129.2.18 -sn -oA host -PE --packet-trace `
`-PE 	            #Performs the ping scan by using 'ICMP Echo requests' against the target.`
`--packet-trace 	#Shows all packets sent and received`

