# EasyPSCP
Python tool for Windows to make PSCP a bit easier.

Why would you use this?:
If you find youself sending files via SSH alot, the pscp command line utility can start taking up alot of time because you will be typing alot of the same values each time. 
This allows you to specify a default port number, username, ip address and save location.


How to use it:
The default script is going to ask alot of questions. Edit the script to load it with the variables you want to save by changing input() to the value you want to use each time.



Configuration Example:

This is the default script:

port_var = "22"
user_var = input("What is the username for the remote machine:\n")
local_file_path_var = input("Drag and drop the local file that you want to send to the target machine into this window:\n")
target_ip_var = input("What is the IP of the target machine?:\n")
target_dir_var = input("What directory do you want to drop the file in on the target machine?:\n")
target_file_name_var = input("What do you want to name the file on the target machine?:\n")


This is the script edited to skip prompting for certain arguments to save time:

port_var = "22"
user_var = "user001"
local_file_path_var = input("Drag and drop the local file that you want to send to the target machine into this window:\n")
target_ip_var = "192.168.1.10"
target_dir_var = (f"/home/{user_var}/")
target_file_name_var = input("What do you want to name the file on the target machine?:\n")
