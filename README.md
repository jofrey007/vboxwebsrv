# Docker vboxwebsrv with server local IP

This is a fork of the [jazzdd86/phpVirtualbox](https://github.com/jazzdd86/vboxwebsrv)

It solve a problem when vboxwebsrv is run on Virtualbox over internet. 

This version adds one more argument 

`-e LOCAL_IP=<ip_address>`

where ip_address is local IP address of server, which runs vboxwebsrv

example:

`docker run -d --name=vbox_websrv --restart=always -e USE_KEY=1 -e SSH_PORT=12222 -e LOCAL_IP=192.168.200.10 -v /home/joe/ssh_keys:/root/.ssh/ user/vboxwebsrv user@10.20.30.40`

Default value of LOCAL_IP is `localhost`
