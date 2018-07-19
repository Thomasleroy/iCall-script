# iCall-script

#1 is an iCall script based on this question : https://devcentral.f5.com/questions/how-to-install-an-icall
The goal is to check if the DNS is able to resolve queries and to automate the process to disable the route advertisment. 
To perfom that we created a pool with two or more DNS root servers and we created DNS monitor to check if the system can access to them throught port 53.
