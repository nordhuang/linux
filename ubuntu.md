
1.  Could not get lock /var/cache/apt/archives/lock - open


Enrico "eNry" Carafa (mr.tennents) at 
https://answers.launchpad.net/ubuntu/+question/181752

referred me to http://askubuntu.com/questions/15433/fixing-could-not-get-lock-var-lib-dpkg-lock. 

sudo fuser -cuk /var/lib/dpkg/lock; sudo rm -f /var/lib/dpkg/lock   (this works)
