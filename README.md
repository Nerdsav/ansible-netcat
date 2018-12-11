# Ansible POC - netcat systemd service

This is an Ansible playbook which creates a static systemd service to start and run netcat on a specified port.


## Version
Uploaded to GitHub repo 2018-12-11


## Documentation

### Setup
1. Host inventory contains a group ncathosts:
```bash
[ncathosts]
server1
server3
```
### Limitations and to-do
1. The playbook has been used and tested against Ubuntu 16.04 servers.

2. The playbook does not work with Python3 which is the default for Ubuntu 16.04. I am still working on this. Python2 needs to be installed on all nodes for now.
```bash
sudo apt update
sudo apt upgrade
sudo reboot
sudo apt install python
```

### Usage
1. Run the playbook to deploy the netcat service
```bash
ansible-playbook ncat_pb.yml
```

2. Login to the server and start the netcat service
```bash
systemctl start ncat@$PORT;.service 
```

3. Verify connection:
```bash
telnet localhost $PORT
```

## License

Copyright (c) 2018 Lester Guerzon &lt;lesterguerzon@pm.me&gt;

Licensed under the GNU GENERAL PUBLIC LICENSE Version 3. See LICENSE in the project root for license information.
