# Ansible Playbook - Netcat service

This is an Ansible playbook which creates a static systemd service to start and run netcat on a specified port.


## Version notes 
Uploaded to GitLab private repo
Date - 2018-10-20


## Documentation
Run the playbook:
> ansible-playbook ncat_pb.yml

Login to the server and start the service.
> systemctl start ncat@&lt;PORT&gt;.service 

Verify connection:
> telnet {server} {port}

## License

Copyright (c) 2018 Lester Guerzon &lt;lesterguerzon@pm.me&gt;

Licensed under the GNU GENERAL PUBLIC LICENSE Version 3. See LICENSE in the project root for license information.
