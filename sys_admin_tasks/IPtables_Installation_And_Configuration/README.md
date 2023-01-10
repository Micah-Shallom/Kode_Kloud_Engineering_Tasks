We have one of our websites up and running on our Nautilus infrastructure in Stratos DC. Our security team has raised a concern that right now Apache’s port i.e 6300 is open for all since there is no firewall installed on these hosts. So we have decided to add some security layer for these hosts and after discussions and recommendations we have come up with the following requirements:



Install iptables and all its dependencies on each app host.

Block incoming port 6300 on all apps for everyone except for LBR host.

Make sure the rules remain, even after system reboot.


