## PhpVirtualBox

This is a container to manage your Virtualbox host with a web interface, is compatible with all version modern version of VirtualBox


## Prerequisites

You need to execute this to start vboxserver:

```
vboxwebsrv -H 0.0.0.0
```

If you want execute in background:

```
vboxwebsrv -H 0.0.0.0 -b
```


## Installation


Example:

```
docker run --name phpvirtual -d -p 80:80  -e ID_HOSTPORT=127.0.0.1:18083 -e ID_NAME=hostname_server -e ID_USER=user_server -e ID_PW=password -e CONF_browserRestrictFolders="/data,/home"  theadribreezy/phpvirtualbox
```
Docker compose:

```
version: '3'
services:
 phpvirtualbox:
    container_name: virtualbox
    image: theadribreezy/phpvirtualbox
    ports:
      - 80:80
    environment:
      - ID_HOSTPORT=127.0.0.1:18083
      - ID_NAME=hostname_server
      - ID_USER=user_server
      - ID_PW=password
      - CONF_browserRestrictFolders="/data,/home"
```

The default pass is:

User: admin

Password: admin

 You can change it after login firts time 

