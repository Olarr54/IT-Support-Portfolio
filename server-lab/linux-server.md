# Ubuntu Server Lab

I previously used VMware Workstation to set up an Ubuntu Server virtual machine as part of a university practical project.

I used the server to practise networking, web hosting, databases, security and troubleshooting.

## Virtual Machine Setup

The Ubuntu Server virtual machine was configured with:

- 2 virtual CPUs
- 2 GB RAM
- 20 GB virtual hard disk
- Ubuntu Server
- VMware Workstation

## Networking

I used:

```bash
ip a

to check the server's network information.

I also configured a static IP address using Netplan. I had an issue with the network configuration initially, so I checked the IP address, subnet and gateway and corrected the settings to match the VMware NAT network.

Web Server

I installed Apache and the other packages needed for a basic LAMP environment.

sudo apt update
sudo apt install apache2 mysql-server php libapache2-mod-php php-mysql

I then tested Apache by accessing the server's IP address from a browser.

I also created a PHP test file in:

/var/www/html

This helped me understand how a Linux server can host a basic web application.

MySQL

I used MySQL to practise database administration.

I ran:

sudo mysql_secure_installation

I then created a database and database user and tested the connection from PHP.

Linux Server Security

I worked with several basic security features in the lab.

UFW

I used UFW to control which network services could access the server.

I allowed the services needed for the web server and SSH while blocking unnecessary access.

User Accounts

I created a normal user account with sudo access rather than using the root account for everyday tasks.

Fail2ban

I also used Fail2ban to monitor repeated login attempts and help protect the server from repeated failed connections.

Problems I Encountered

One problem involved PHP and MySQL not working correctly together. I checked the code and found issues with variable names and missing semicolons.

I also had problems with the static IP configuration. I checked the network information using ip a and reviewed the Netplan configuration before correcting the subnet and gateway.

These problems helped me understand that checking the error and working through the problem step by step is usually more useful than changing lots of settings at once.

What I Learned

This practical gave me experience with:

Linux server administration
Basic networking
Apache web servers
MySQL databases
PHP
User permissions
Firewall configuration
SSH
Basic server security
Troubleshooting configuration problems

The main thing I learned was to check the symptoms, look at the relevant configuration or error message, make one change at a time and then test the result.