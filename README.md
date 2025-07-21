# Cisco Lab Project

This project provides a set of container-based network lab topologies using `containerlab`. It is designed for network engineers and learners to simulate, test, and automate network scenarios with Cisco IOS, IOSvL2, and Arista cEOS devices.

## Project Structure

- **ceos.clab.yaml**: Arista cEOS topology definition.
- **cisco.clab.yml**: Cisco lab topology (version 1) definition.
- **cisco_02.clab.yml**: Cisco lab topology (version 2) definition.

## Topologies

### Arista cEOS Topology (`ceos.clab.yaml`)
- Two cEOS nodes (ceos1, ceos2) connected via eth1.

### Cisco Lab Topologies
- **cisco.clab.yml** and **cisco_02.clab.yml** define labs with:
  - R1: Cisco IOSv router
  - D1: Cisco IOSvL2 device
  - S1, S2: Cisco IOL Layer 2 switches
  - Various links between devices

![lab](/screenshot.png)

## Usage

1. **Install Containerlab**
   - Follow instructions at https://containerlab.dev/install/

2. **Deploy a Topology**
   - Example: `containerlab deploy -t cisco_02.clab.yml`

## Credentials
- Default username/password for devices: `admin/admin`

## Notes
- Requires Docker and Containerlab.
- Images referenced must be available locally or via Docker Hub.
- SSH keys and configs are provided for convenience.

## References
- [Containerlab Documentation](https://containerlab.dev/)
- [Cisco IOL Images](https://github.com/vrnetlab/vrnetlab)
- [Arista cEOS Images](https://www.arista.com/en/)

## License
This project is for educational and testing purposes only. Use Cisco and Arista images in accordance with their respective licenses.
