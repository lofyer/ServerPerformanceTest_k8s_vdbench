# Example procedures and helper scripts for installing and executing workload benchmark.

Please note partners might need to make customization to the scripts below for their own deployment environment.

Default VM Operating System: CentOS 7.6.

# Helper Scripts 

Please review and check the content of the script (and make necessary changes) before running.

* Create server VMs with volume attached, and generate files for ansible run (For use as VDBench and Redis instances)

  ./scripts/create_servers.sh $num-of-vms $num-of-vols-per-vm

* Clean up all the server VMs and volumes

  ./scripts/delete_server.sh 

* Create client VMs with volume attached, and generate files for ansible run (For use as memtier clients)

  ./scripts/create_clients.sh $num-of-vms $num-of-vols-per-vm

* Clean up all the client VMs and volumes

  ./scripts/delete_clients.sh 

* Display # VMs for each hypervisor

  ./scripts/vmstat.sh

* Reference procedure to install OpenStack Rally

  ./scripts/install_rally.sh

* Reference procedure to create OpenStack compute flavor for redis and memtier

  ./scripts/create_redis_flavors.sh

* Reference procedure to install memtier (1-1 redis-memtier server-client mapping)

  ./scripts/python memtier.py
