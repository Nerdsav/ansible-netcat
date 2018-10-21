# Ansible Playbook - Netcat systemd service

This is an Ansible playbook which creates a static systemd service to start and run netcat on a specified port.


## Version notes 
Uploaded to GitLab private repo
Date - 2018-10-20


## Documentation

### Notes
This playbook is designed and tested on a standard Ubuntu 16.04 installation.

### Usage
1. Run the playbook to deploy the netcat service
> ansible-playbook ncat_pb.yml

2. Login to the server and start the netcat service
> systemctl start ncat@&lt;PORT&gt;.service 

3. Verify connection:
> telnet {server} {port}


## License

Copyright (c) 2018 Lester Guerzon &lt;lesterguerzon@pm.me&gt;

Licensed under the GNU GENERAL PUBLIC LICENSE Version 3. See LICENSE in the project root for license information.
