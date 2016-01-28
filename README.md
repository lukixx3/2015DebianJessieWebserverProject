# 2015DebianJessieWebserverProject
A setup script for a Debian LAMP Webserver.
Building with a security focus & geared towards higher performance than stock.


Initially this will be in implemented with bash until I arrive at an end result I am happy with.

I will use the bash script as a roadmap to build an Ansible playbook.

Bear in mind this is very much in progress.

#How to use this:

\#1 Start up a blank linode, initially provision it with Debian 8.1

\#2 SSH into the machine

\#3 cut/paste this mess into the command line:
`wget https://raw.githubusercontent.com/bradchesney79/2015DebianJessieWebserverProject/master/init.sh && chmod 770 init.sh && ./init.sh && cd /root/bin`

\#4 set up a junk email service, I reccomend [http://33mail.com](http://33mail.com) -- they even have a configuration for people like us in the works

\#5 edit setup.conf with your hosts particulars you'll _need_ to edit a few things:
`IPV4=<your linode IPV4 address>`

`IPV6=<your linode IPV6 address>`

`TARGETEMAIL=<your email with the junk email service>` 

\#6 then cut/paste this in the command line to run these two scripts:
`. /root/bin/build-script.sh && . /root/bin/load-script.sh`

TODO:

finish configuring sentinel

configure global webdev resources like composer, node, fonts to run tests & builds

improve troubleshooting resources

remedy broken GUI SFTP -- works fine CLI

update troubleshooting resources on github

improve readability

break into modular Ansible scripts


NICE TO HAVE:

disk partitions

THANKS:

simplified logging - http://reddit.com/user/cheaphomemadeacid


For me to test the whole thing as-is:

`wget https://raw.githubusercontent.com/bradchesney79/2015DebianJessieWebserverProject/master/init.sh && chmod 770 init.sh && ./init.sh && cd /root/bin && . /root/bin/build-script.sh && . /root/bin/load-script.sh`


##Takes ... on a Linode 1024:

real   11m24.996s

real   15m28s 
