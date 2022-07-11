Before start the script you need to create a ssh key to authorize ssh without give password

Command: ssh-keygen -t rsa

The default output will be id_rsa and id_rsa.pub
You need to upload the id_rsa.pub at the end of the file /home/myuser/.ssh/authorized_keys

After validate the ssh without password for all servers that you need to connect follow the instructions below:


Files
Script: os-version.sh
Output: server_version.txt
Server list: myservers_list.txt

How to Run
./os-version.sh myservers_list.txt

Result
After the script ran you will have a file server_version.txt
