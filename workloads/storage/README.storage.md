# Storage Benchmark 

Please review and check the content of the script (and make necessary changes) before running.

1. (Optional)For OpenStack: launch 30 VMs m1.large (CentOS 7.6, 4 vCPU, 8GB RAM), attach 2x 50GB volume for each VM. 

   ./scripts/create_servers.sh 30 2

2. Install and run VDBench on each VMs

   yum install -y ansible
   cp -r ansible/roles/vdbench /usr/share/ansible/roles/
   cd scripts
   ansible-playbook -i servers ../ansible/example/vdbench.yaml

3. Install VDBench on Master VM

   yum install -y java-1.8.0-openjdk

6. Run VDBench benchmark with parameter file

   unzip vdbench.zip 
   cd vdbench
   ./vdbench -f iss.param -o output-result-dir

