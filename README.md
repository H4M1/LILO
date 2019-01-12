# LILO
Locate ILO (LILO) (HP Integrated Lights-Out) On you local network by scanning known ports

lilo - Search a local network segment for iLOs

            The iLO is the Integrated Lights-Out management processor
            
            used on HP ProLiant and BladeSystem servers

 Requires: tr sed expr curl nmap

 Tested with: Nmap 4.20, curl 7.17.1, RHEL4

 Note: Discovery of an iLO is dependent upon the Virtual Media port
       being set to the default of 17988.  If this has been changed
       by the iLO administrator, then this script will NOT find it.

       Also, if the iLO XML Reply Data Return has been Disabled by
       the iLO administrator, this script will not be able to
       gather any information about the server.  It will still be
       discovered, but all you will see is its IP address.

 USAGE:
 sudo ./lilo {target network specification}
 
 TARGET NETWORK SPECIFICATION:

  Can pass hostnames, IP addresses, networks, etc.
  
  Ex: server1.company.com, company.com/24, 192.168.0.1/16, 10.0.0-255.1-254
  
EXAMPLE:
  sudo ./lilo 16.32.64.0/22
