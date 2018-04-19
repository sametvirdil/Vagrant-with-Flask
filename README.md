How to Use Vagrant Environment Guide

1.	Install Vagrant from the below link for your OS, here we will use Windows version of it. You need also VirtualBox installed on your machine besides that.
http://www.vagrantup.com/downloads.html
2.	Create a directory for your Vagrant box, e.g. 1vagbox  and under this dir on the console run command “ vagrant init ubuntu/trusty64 ” and this command will download required image automatically and place a Vagrantfile into this directory. 
3.	Copy the provided vagrantfile (this will replace the existing one) and bootstrap.sh script files provided into the folder of Vagrant machine 1vagbox
4.	Also create a directory named www under the 1vagbox folder and copy hello.py app file into this from the below github link 
https://github.com/sametvirdil/assignment/ 
5.	vagrant up command under this 1vagbox folder will bring up the related vagrant box VM.  During initalizing the vagrant machine, the installation of the required python-pip and flask packages will also be automatically installed with the help of the bash script under the corresponding folder of 1vagbox.
6.	Wait during the vagrant up command finishes all the required tasks and after completion you may check from your browser with the url below
http://localhost:5050/  and  see your app running
