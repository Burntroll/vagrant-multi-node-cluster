## Multi-Node Docker Swarm Cluster with Vagrant

This repository contains files to set up a Vagrant environment with multiple Ubuntu 22.04 machines that have Docker and Docker Compose installed. There are four machines defined in the Vagrantfile - a master and three nodes. The master machine has Docker Swarm initialized, and the worker.sh file is generated for each worker node, which is then used by the worker.sh script to join the swarm.

### Prerequisites

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)

### Installation

1. Clone the repository: `git clone https://github.com/Burntroll/vagrant-multi-node-cluster.git`
2. Navigate to the cloned directory: `cd vagrant-multi-node-cluster`
3. Run `vagrant up` command to start the virtual machines.
4. Wait for the installation to finish.

### Usage

1. To ssh into the master machine, run `vagrant ssh master`.
2. To ssh into the worker nodes, run `vagrant ssh node01`, `vagrant ssh node02`, `vagrant ssh node03`.
3. To stop the virtual machines, run `vagrant halt`.
4. To remove the virtual machines, run `vagrant destroy`.

### Files

- Vagrantfile: This file defines the virtual machines and their configurations.
- docker.sh: This file installs Docker and Docker Compose.
- master.sh: This file initializes the Docker Swarm on the master node.
- worker.sh: This file joins the worker nodes to the Docker Swarm.

### Contributing

Contributions to this repository are welcome. Before submitting a pull request, please ensure that your changes are well-tested and aligned with the existing code style.

### License

This repository is licensed under the MIT license.
