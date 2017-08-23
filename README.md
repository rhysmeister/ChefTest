A simple setup to create an virtual environment to play with Chef Automate as outlines at the folowing url: https://learn.chef.io/modules/chef-automate-pilot/scan-for-compliance#/

Please ensure Vagrant, VirtualBox, Ansible and git are installed before proceeding. 

Requirements
=============

Minimum versions;

* vagrant 1.9.0
* virtualbox 5.0.26 r108824
* ansible 2.2.0.0
* git version 2.11.0

Getting Started
===============

```
git clone https://github.com/rhysmeister/ChefTest.git
cd ChefTest
vagrant up
```

This will take sometime the first time it is executed as an entire Chef environment has to be downloaded.

Once the process has completed sucessfully you can access the webfront end with the following url;

http://192.168.50.4

Login with default credentials;

u: admin
p: password

To execute the additonal docker command mentioned in the tutorial you should do that from inside the Vagrant created VM.

From the ChefTest project folder cloned from git;

```
vagrant shh
sudo docker run chefdemo/compliance-loader-pass:stable
```
