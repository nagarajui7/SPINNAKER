# SPINNAKER

1) Edit /etc/apache/ports.conf and remove change Listen 127.0.0.1:9000 to Listen 9000 
1a) Add a reverse proxy for ports you wish to open in Apache 
2) You may edit service files in /opt/spinnaker/conf to disable the bind to local host. Change localhost to domain name or 0.0.0.0

I got it working by also changing 127.0.0.1:9000 to *:9000 in /etc/apache2/sites-enabled/spinnaker.conf.
#sudo bash ~/SPINNAKER/scripts/6-restart-spinnaker.sh

go to /opt/spinnaker/conf
#cd /opt/spinnaker/conf
#sed -i 's/localhost/0.0.0.0/' *
#sudo bash ~/SPINNAKER/scripts/6-restart-spinnaker.sh

