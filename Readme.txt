This playbook is my first encounter with Ansible, and I can see that it is very powerful.

*****************************
Version 2
See below for previsous Version

There were some cut & paste errors in the playbook which have been corrected
and I messed up the Virtualhosts tag 
and I was going to use GitHub but changed my mind for speed, for the personal key and had the wrong label in the playbook

To use this playback there are some things you will need to do:

1) Add the host IP to Ansible’s inventory file “hosts” and allow SSH access by copying the public key that Ansible uses in the approved way

2) Copy the self-signed keys in the Github project to a folder on the machine running Ansible  which needs to be called /root/sslcerts
The files are: ca.crt, ca.csr, & ca.key - and also copy strudwick.pub to the same place

3) on the target machine you will need: yum install libselinux-python


**************************
Version 1

I have had only a little time to pull together the project asked for in this test, and I have had to cut a few corners to get something coherent delivered. 

I only got the spec late on Monday, and was not able to start until Tuesday ( yesterday evening ) – I have never used Ansible before.

There are many more things I would like to do if this was a real project and have a least enjoyed the journey so far. 
Examples are not using root, pulling more things out into variables and so forth. 

To use this playback there are some things you will need to do:

1) Add the host IP to Ansible’s inventory file “hosts” and allow SSH access by copying the public key that Ansible uses in the approved way

2) Copy the self-signed keys in the Github project to a folder on the machine running Ansible  which needs to be called /root/sslcerts
The files are: ca.crt, ca.csr, & ca.key - 
*** Version 2 addition - 
so also copy strudwick.pub to the same place

3) Edit the line in the playbook to suit the IP address of the target machine, changing 192.168.0.101 with the correct IP
action: shell /bin/echo '<VirtualHost *:443 192.168.0.101>' >> /etc/httpd/conf/httpd.conf

Apologies that I did not have time to do these things in a more elegant way.

John Strudwick
Wednesday 11th February 2015

