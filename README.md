# OpenvpnTutorial

This is a simple repository about how I learn Openvpn on a Ubuntu Server provided by Google Clound.     

One reason i created this is to help myself remember the flow.  Besides, I want to help those who struggle    
with Openvpn and Clound Server.   

## Google Clound

Google Clound is very strong but complicated. First time we use Google Clound, I don't know what to do.      

1. When we create the instance, we need to have **Allow full access to all Cloud APIs** in **Identity and API access**   
this will help us transfer file from remote to local.  

 

## Server setting

1. change to the root user `sudo su root`  

2. change the root password `passwd`   

3. change the user password using root user `passwd username`    

this will save us in the future, since google clound have no default password. but sometimes we need password to do sudo action.    

4. install wget  `sudo apt install wget`     

## Installation   

1. Download the shell script provided by [Nyr](https://github.com/Nyr/openvpn-install) `wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh`.    

2. Change script into excutable `sudo chmod +x openvpn-install.sh`    

3. Run the script using sudo `sudo ./openvpn-install.sh`     

It is ok to use the default setting for the installation.

## Tranfer file from server to local   

1. Create a bucket in **clound storage** in the **Storage** part.  

2. Using the `gsutil cp yourfile.txt gs://your-bucket`
