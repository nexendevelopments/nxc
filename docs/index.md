## NEXENCloud

NEXENCloud is a web interface for managing instances of LXD.

Its recomended that you install NEXENCloud in a container or virtual machine to avoid
clutering your system, it installs alot of dependencies (mysql, apache, node)

### Documentation

The majority of what will be covered in this documentation is specific to NEXENCloud
and not LXD itself, you can read the documentation for lxd <a href="https://lxd.readthedocs.io/" target="_blank"> Here </a>

### Installing NEXENCloud Ubuntu
```
# Launch a ubuntu container
lxc launch ubuntu: nexenCloud
# Connect to ubuntu console
lxc exec nexenCloud bash
#  Download the script
curl https://raw.githubusercontent.com/turtle0x1/NexenCloud/master/examples/install_with_clone.sh >> installNexenCloud.sh
# Then give the script execution permissions
chmod +x installNexenCloud.sh
# Then run bellow to setup the program
./installNexenCloud.sh
```
### Installing NEXENCloud Centos 7
```
# Launch a centos 7 container
lxc launch images:centos/7/amd64 nexenCloud
# Connect to centos console
lxc exec nexenCloud bash
# Download the script
curl https://raw.githubusercontent.com/turtle0x1/NexenCloud/master/examples/install_with_clone_centos7.sh >> installNexenCloud.sh
# Then give the script execution permissions
chmod +x installNexenCloud.sh
# Then run bellow to setup the program
./installNexenCloud.sh
```

### Post Installation
Once the installation is complete you need to go to into your browser and vist;

`https://container_ip_address`

and accept the self signed certificate, you will then be able to enter your LXD instance
details.
