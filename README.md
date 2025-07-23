# Containerlab Project -- Cisco Devices

This project provides a set of container-based network lab topologies using `containerlab`. It is designed for network engineers and learners to simulate, test, and automate network scenarios with Cisco IOS, IOSvL2, devices.

## Topologies

### Cisco Lab Topologies

- **cisco_01.clab.yml** and **cisco_02.clab.yml** define labs with:
  - R1: Cisco IOSv router
  - D1: Cisco IOSvL2 device
  - S1, S2: Cisco IOL Layer 2 switches
  - Various links between devices

![lab](/screenshot.png)

## Usage

1. **Install Containerlab**
   - Follow instructions at https://containerlab.dev/install/#install-script

2. **Deploy a Topology**
   - Example: `containerlab deploy -t cisco_02.clab.yml`
   - It will pull images from my [Docker Hub](https://hub.docker.com/u/asifsyd) repo.

3. **Automate with Nornir**
   This project leverages Nornir for network automation tasks. The Nornir inventory is configured using `config.yaml`, `hosts.yaml`, `groups.yaml`, and `defaults.yaml`.

   To run a Nornir script, ensure you have Nornir and `nornir_netmiko` installed in your Python environment.

   Example: Run the `show_intf_description.py` script to display interface brief information from the deployed devices:
   ```bash
   python show_intf_description.py
   ```

## Credentials
- Default username/password for devices: `admin/admin`

## Notes
- Requires Docker and Containerlab.
- Images referenced must be available locally or via Docker Hub.
- SSH keys and configs are provided for convenience.

## License
This project is for educational and testing purposes only. Use Cisco and Arista images in accordance with their respective licenses.
