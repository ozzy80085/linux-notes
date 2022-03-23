   
 ## start a socks proxy with ssh

	ssh -N -D 0.0.0.0:1080 localhost

## run is background as a daemon
    ssh -f -N -D 0.0.0.0:1080 localhost
  

## you can also use another computer running ssh as an exit node (where the traffic leaves and goes to the internet)
 
	ssh -f -N -D 1080 other_computer.com

This will set up a SOCKS5 proxy on  `localhost:1080`  but when you use it, ssh will automatically tunnel your requests (encrypted) via  `other_computer.com`. This way you can hide what you're doing on the Internet from anyone who might be sniffing your link. They will see that you're communicating with  `other_computer.com`  but the traffic will be encrypted so they won't be able to tell what you're doing.



more shit here: https://catonmat.net/linux-socks5-proxy
