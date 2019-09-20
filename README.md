# fail2ban_setup

My jails and actions for banning IPs on my virtual machines.

The jails and pretty self explanatory and really didn't even need to be included but hey, there they are. If 5 failed login attempts occur within a 4 hour window the IP is banned for one hour. If an IP is banned twice within 24 hours then it is added to a permanent blacklist.

The action.d/ files handles the banning. Currently it just issues an ssh command to the server acting as the firewall to add the ip to one of two ipset lists depending on the jail triggered.
