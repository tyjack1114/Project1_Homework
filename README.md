# Project1_Homework
Repository for the Week 13 Project

  Day 1
  =====
   1. I created a new Virtual Network named ELK-NET
   ..* ELK-NET was placed in the (US) West region
   2. A peering was created that was named ELK-to-RED
   ··2. ELK-NET has been peered to the RedTeamVNET 
   ··3. The peering from RedTeamVNET to ELK-NET is named RED-to-ELK
   3. I then proceeded to SSH into the Jump-Box VM 
   ··2. Started and connected to the Ansible container
   ··3. After connecting to Ansible I retrieved the SSH key of my other VMs
   ··4. Now I started configuring my new VM named ELK-SERVER *username is sysadmin*
     ..* The ELK-SERVER VM is located in the (US) West region
     ..* The new VM Image is on Ubuntu 18.04 LTS, with 2 vcpus and 8GiB memory
   4. At this point I added the new VMs private IP *10.1.0.4* to the Ansible hosts file
   5. I then had to create an Ansible playbook for the new ELK VM
   ··2. The final syntax that I used for the playbook is stated in the ansible folder
   6. After writing the Ansible playbook I ran the command *ansible-playbook elk.yml* 
   7. I then made sure the ELK container was running properly
   ..* SSH into ELK VM and run the command *docker ps*
   8. Had to make a Security rule that allowed all traffic into the ELK-SERVER 
   ..* Just the port 80 rule alone would not allow my VM to load on Google or Internet Explorer
   ..* Looking up *http://**VMPublicIP**:5601/app/kibana* on Google will load with the current configuration
   
   
  Day 2
  ===== 
   1. At the beginning of Day 2 I navigated to my ELK VM and started my Ansible container
   ..* After navigating to the ELK VM I then went to the *Add Log Data* tab
   ..* From there I chose *System Logs* and clicked on the DEB tab
   2. Once under that tab I went back to my Ansible container to configure and install Filebeat
   ··2. I installed a template of the Filebeat Configuration file 
   ··3. The changes that were made to the file  are on line #1106 and line #1806
   ··4. Once the conifgurations were made I saved this file /etc/ansible/filebeat-config.yml
   
   3. I then had to make a Filebeat Playbook, the correct configuration and syntax is located in
      the ansible folder 
   4. Finally after writing the playbook correctly I ran the following command
   ..* *ansible-playbook filebeat-playbook.yml*
   5. To conclude the project I went back to my ELK VM and clicked Check Data 
   ..* The Check Data button is located under the Module Status
   

  
   
   
   
