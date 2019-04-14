
# Ansible proof-of-concept - netcat systemd service

This project consists of a simple Ansible playbook which creates a static systemd service to start a dummy service on a specified port using `netcat`.

## Limitation

The playbook is for Red Hat Enterprise Linux 7 targets (and derivatives).

## Usage

1. Identify the IP address of the target and the desired port.

    ```bash
    echo 192.168.56.68 > hosts
    export port=1234
    ```

2. Run the playbook to deploy and start the service.

    ```bash
    ansible-playbook -i hosts -e "listenport=$port" ncat_pb.yml
    ```

3. The playbook performs the test, but you can also verify using the following command:

    ```bash
    nc -zv 192.168.56.68 $port
    ```

## License

Copyright (c) [Lester Guerzon](mailto:lester@ilesterg.net); See [LICENSE](./LICENSE) for more information.
