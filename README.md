How to Use Vagrant Environment Guide
Installation of the Environment
1.	Install Vagrant from the below link for your OS, here we will use Windows version of it. We will  need also VirtualBox installed on your machine besides that.
http://www.vagrantup.com/downloads.html
2.	Create a directory for your Vagrant box, e.g. 1vagbox  and under this dir on the console run command “ vagrant init ubuntu/trusty64 ” and this command will download required image automatically and place a Vagrantfile into this directory. 
3.	Copy the provided vagrantfile (this will replace the existing one) and bootstrap.sh script files provided into the folder of Vagrant machine 1vagbox
4.	Also create a directory named www under the 1vagbox folder and copy hello.py app file into this from the below github link 
https://github.com/sametvirdil/Vagrant-with-Flask
5.	vagrant up command under this 1vagbox folder will bring up the related vagrant box VM.  During initalizing the vagrant machine, the installation of the required python-pip and flask packages will also be automatically installed with the help of the bash script under the corresponding folder of 1vagbox.
6.	Wait during the vagrant up command finishes all the required tasks and after completion you may check from your browser with the url below
http://localhost:5555/  and  see your app running


Some change or update to the Flask app code

If we try to change or add anything inside the hello.py file; for example consider some change to the text inside return string between double  quotation marks; we will first need to kill existing flask app. In order to find its process id pid; use command

ps waux |grep flask 

 

And after finding the pid number give command sudo kill 1691 where you put the corresponding pid instead 1691

 


 Now we only need to run the 2 line commands below in order to see the changes to the Flask app code:

export FLASK_APP=/var/www/hello.py
flask run --host=0.0.0.0 &


Some Basic Info About Vagrant Usage

vagrant halt command stops a Vagrant machine, we may use with -f  parameter when needed to force to stop.

vagrant reload command stops and then restarts a Vagrant machine. If any change made to the Vagrantfile a reload should be called since needed to detect the changes made.

